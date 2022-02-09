<script setup lang="ts">
import { computed, toRefs } from 'vue'

export interface Props {
  label: string
  width: string
  type: HTMLButtonElement
  color?: 'primary' | 'secondary' | 'disabled'
  outlined?: boolean
}

interface Emits {
  (event: 'close'): void
}

const props = defineProps<Props>()
const { label, width, type, color, outlined } = toRefs(props)

const emit = defineEmits<Emits>()

const onClick = () => {
  emit('close')
}

const classObject = computed(() => {
  return {
    outlined: outlined?.value,
    text: !outlined?.value,
    primary: color?.value === 'primary',
    secondary: color?.value === 'secondary',
  }
})
</script>

<template>
  <button :type="type" :class="['close-button', classObject]" @click="onClick">
    {{ label }}
  </button>
</template>

<style scoped>
.close-button {
  cursor: pointer;
  border-radius: 4px;
  font-weight: bold;
  min-height: 40px;
  width: v-bind(width);
  transition: opacity 0.2s;
  display: flex;
  align-items: center;
  justify-content: center;
}

.close-button:hover {
  opacity: 0.8;
}

.outlined {
  border: 1px solid #e2e8f0;
}

.text {
  border: none;
  transition: opacity 0.2s;
}

.text:hover {
  background-color: #e2e8f0;
}

.primary {
  background-color: #2b6cb0;
  color: white;
}

.secondary {
  background-color: #e2e8f0;
}
</style>

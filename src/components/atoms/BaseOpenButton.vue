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
  (event: 'open'): void
}

const props = defineProps<Props>()
const { label, width, type, color, outlined } = toRefs(props)

const classObject = computed(() => {
  return {
    outlined: outlined?.value,
    text: !outlined?.value,
    primary: color?.value === 'primary',
    secondary: color?.value === 'secondary',
  }
})

const emit = defineEmits<Emits>()

const onClick = () => {
  emit('open')
}
</script>

<template>
  <button :type="type" :class="['open-button', classObject]" @click="onClick">
    {{ label }}
  </button>
</template>

<style scoped>
.open-button {
  cursor: pointer;
  border-radius: 4px;
  font-weight: bold;
  min-height: 40px;
  width: v-bind(width);
  transition: opacity 0.2s;
  border: 1px solid #e2e8f0;
  background-color: #e2e8f0;
  display: flex;
  align-items: center;
  justify-content: center;
}

.open-button:hover {
  opacity: 0.8;
}
</style>

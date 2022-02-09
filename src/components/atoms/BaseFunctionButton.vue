<script setup lang="ts">
import { computed, toRefs } from 'vue'

interface Props {
  label: string
  width: string
  type: HTMLButtonElement
  color?: 'primary' | 'secondary' | 'disabled'
  outlined?: boolean
}

const props = defineProps<Props>()
const { label, width, type, color, outlined } = toRefs(props)

const secondaryAction = () => {
  console.log('hoge')
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
  <button
    :type="type"
    :class="['function-button', classObject]"
    @click="secondaryAction"
  >
    {{ label }}
  </button>
</template>

<style scoped>
.function-button {
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

.function-button:hover {
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

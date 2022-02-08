<script setup lang="ts">
import { computed, toRefs } from 'vue'

interface Props {
  label: string
  type: HTMLButtonElement
  color?: 'primary' | 'secondary' | 'disabled'
  outlined: boolean
  width: string
}

const props = defineProps<Props>()
const { label, type, color, outlined, width } = toRefs(props)

const outlinedClass = computed(() => {
  return {
    outlined: outlined.value,
    text: !outlined.value,
    primary: color?.value === 'primary',
    secondary: color?.value === 'secondary',
  }
})
</script>

<template>
  <button :type="type" :class="['button', outlinedClass]">
    {{ label }}
  </button>
</template>

<style scoped>
.button {
  cursor: pointer;
  border-radius: 4px;
  transition: opacity 0.2s;
  width: v-bind(width);
  min-height: 40px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: bold;
}

.button:hover {
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

<script setup lang="ts">
import { toRefs } from 'vue'

interface Props {
  label: string
  type: HTMLButtonElement
  color: 'primary' | 'secondary' | 'disabled'
  outlined: boolean
}

const props = defineProps<Props>()
const { label, type } = toRefs(props)
</script>

<template>
  <button :type="type">
    {{ label }}
  </button>
</template>

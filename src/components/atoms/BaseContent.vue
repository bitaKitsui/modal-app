<script setup lang="ts">
import { toRefs } from 'vue'

interface Props {
  value: string
}

const props = defineProps<Props>()
const { value } = toRefs(props)
</script>

<template>
  <p>{{ value }}</p>
</template>

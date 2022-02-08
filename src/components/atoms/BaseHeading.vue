<script setup lang="ts">
import { toRefs } from 'vue'

interface Props {
  value: string
}

const props = defineProps<Props>()
const { value } = toRefs(props)
</script>

<template>
  <h4>{{ value }}</h4>
</template>

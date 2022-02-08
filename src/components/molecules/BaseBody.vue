<script setup lang="ts">
import BaseContent from '../atoms/BaseContent.vue'
import { toRefs } from 'vue'

interface Props {
  body: string
}

const props = defineProps<Props>()
const { body } = toRefs(props)
</script>

<template>
  <div class="body">
    <BaseContent :value="body" />
  </div>
</template>

<style scoped>
.body {
  margin: 10px 0;
}
</style>

<script setup lang="ts">
import { toRefs } from 'vue'
import BaseHeading from '../atoms/BaseHeading.vue'
import BaseCloseButton from '../atoms/BaseCloseButton.vue'

interface Props {
  headerTitle: string
}

const props = defineProps<Props>()
const { headerTitle } = toRefs(props)
</script>

<template>
  <div class="header">
    <BaseHeading :value="headerTitle" />
    <BaseCloseButton
      :label="'×'"
      :type="'button'"
      :outlined="false"
      :width="'40px'"
    />
  </div>
</template>

<style scoped>
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
</style>

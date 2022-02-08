<script setup lang="ts">
import BaseHeading from '../atoms/BaseHeading.vue'
import BaseButton from '../atoms/BaseButton.vue'
import { toRefs } from 'vue'

interface Props {
  headerTitle: string
}

const props = defineProps<Props>()
const { headerTitle } = toRefs(props)
</script>

<template>
  <div class="header">
    <BaseHeading :value="headerTitle" />
    <BaseButton
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

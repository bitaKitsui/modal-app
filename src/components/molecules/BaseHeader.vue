<script setup lang="ts">
import BaseHeading from '../atoms/BaseHeading.vue'
import BaseButton from '../atoms/BaseButton.vue'
</script>

<template>
  <div class="header">
    <BaseHeading :value="'Modal Title'" />
    <BaseButton
      :label="'×'"
      :type="'button'"
      :color="'secondary'"
      :outlined="false"
    />
  </div>
</template>

<style scoped>
.header {
  display: flex;
  justify-content: space-between;
}
</style>

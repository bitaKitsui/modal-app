<script setup lang="ts">
import BaseCloseButton from '../atoms/BaseCloseButton.vue'
import BaseFunctionButton from '../atoms/BaseFunctionButton.vue'
</script>

<template>
  <div class="footer">
    <BaseCloseButton
      :label="'Close'"
      :type="'button'"
      :color="'primary'"
      :outlined="true"
      :width="'70px'"
    />
    <BaseFunctionButton
      :label="'Secondary Action'"
      :type="'button'"
      :outlined="false"
      :width="'170px'"
    />
  </div>
</template>

<style scoped>
.footer {
  display: flex;
  justify-content: flex-end;
}
</style>

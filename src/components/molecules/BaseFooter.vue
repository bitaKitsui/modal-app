<script setup lang="ts">
import BaseButton from '../atoms/BaseButton.vue'
</script>

<template>
  <div class="footer">
    <BaseButton
      :label="'Close'"
      :type="'button'"
      :color="'primary'"
      :outlined="true"
      :width="'70px'"
    />
    <BaseButton
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

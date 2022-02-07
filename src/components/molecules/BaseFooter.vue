<script setup lang="ts">
import BaseButton from '../atoms/BaseButton.vue'
</script>

<template>
  <div>
    <BaseButton
      :label="'Close'"
      :type="'button'"
      :color="'primary'"
      :outlined="true"
    />
    <BaseButton
      :label="'Secondary Action'"
      :type="'button'"
      :color="'secondary'"
      :outlined="false"
    />
  </div>
</template>

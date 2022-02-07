<script setup lang="ts">
import BaseHeader from '../atoms/BaseHeader.vue'
import BaseButton from '../atoms/BaseButton.vue'
import BaseContent from '../atoms/BaseContent.vue'
</script>

<template>
  <div>
    <BaseHeader :value="'Modal Title'" />
    <BaseButton
      :label="'×'"
      :type="'button'"
      :color="'secondary'"
      :outlined="false"
    />
    <BaseContent
      :value="'Sit nulla est ex deserunt exercitation anim occaecat.'"
    />
  </div>
</template>

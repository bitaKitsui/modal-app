<script setup lang="ts">
import { toRefs } from 'vue'
import BaseBody from '../molecules/BaseBody.vue'
import BaseFooter from '../molecules/BaseFooter.vue'
import BaseHeader from '../molecules/BaseHeader.vue'
import { MODAL_BODY } from '../../constants'

interface Props {
  isActive: boolean
}

interface Emits {
  (event: 'close'): void
}

const props = defineProps<Props>()
const { isActive } = toRefs(props)

const emit = defineEmits<Emits>()

const handleClose = () => {
  emit('close')
}
</script>

<template>
  <div v-if="isActive" class="modal">
    <BaseHeader :header-title="'Modal Title'" @close="handleClose" />
    <BaseBody :body="MODAL_BODY" />
    <BaseFooter @close="handleClose" />
  </div>
</template>

<style scoped>
.modal {
  padding: 10px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  border: 1px solid;
  border-radius: 4px;
  min-height: 300px;
}
</style>

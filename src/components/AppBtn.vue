<template>
  <button class="btn" :class="computedClass">
    {{ label }}

    <img v-if="iconURL" :src="iconURL" alt="arrow right icon" class="img" />
  </button>
</template>

<script setup lang="ts">
import { computed } from 'vue'

type Props = {
  label: string
  iconURL: string
  backgroundColor: string
  textColor: string
  borderColor: string
  fullWidth: boolean
}

const props = defineProps<Props>()

const computedClass = computed(() => {
  return [
    `${props.backgroundColor} ${props.textColor} ${props.borderColor}`,
    `${props.fullWidth && 'w-full'}`
  ].join(' ')
})
</script>

<style scoped>
.btn {
  @apply flex justify-center items-center gap-2 px-7 py-4 border font-montserrat text-lg leading-none rounded-full;
}
.img {
  @apply ml-2 rounded-full bg-white w-5 h-5;
}
</style>

<template>
  <div
    class="border-2 rounded-xl cursor-pointer max-sm:flex-1"
    :class="computedClass"
    @click="handleClick"
  >
    <div
      class="flex justify-center items-center bg-card bg-center bg-cover sm:w-40 sm:h-40 rounded-xl max-sm:p-4"
    >
      <img
        :src="imgURL?.thumbnail"
        :width="127"
        height="103.34"
        alt="shoe colletion"
        class="object-contain"
      />
    </div>
  </div>
</template>

<script setup lang="ts">
import { computed } from 'vue'

type Props = {
  imgURL: {
    thumbnail: string
    bigShoe: string
  }
  bigShoeImg: string
}

type Emits = {
  (e: 'changeBigShoeImage', newImage: string): void
}
const props = defineProps<Props>()
const emits = defineEmits<Emits>()

const computedClass = computed(() => {
  return props.bigShoeImg === props.imgURL.bigShoe ? 'border-coral-red' : 'border-transparent'
})

const handleClick = () => {
  /* if (bigShoeImg !== imgURL.bigShoe) {
      changeBigShoeImage(imgURL.bigShoe);
    } */

  if (props.bigShoeImg !== props.imgURL.bigShoe) {
    emits('changeBigShoeImage', props.imgURL.bigShoe)
  }
}
</script>

<style lang="scss" scoped></style>

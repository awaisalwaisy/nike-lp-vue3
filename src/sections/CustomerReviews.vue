<template>
  <section class="max-container">
    <h3 class="font-palanquin text-center text-4xl font-bold">
      What Our
      <span class="text-coral-red"> Customers </span>
      Say?
    </h3>
    <p class="m-auto mt-4 max-w-lg text-center info-text">
      Hear genuine stories from our satisfied customers about their exceptional experiences with us.
    </p>

    <div class="mt-24 flex flex-1 justify-evenly items-center max-lg:flex-col gap-14">
      <ReviewCard v-for="review in reviews" :key="Number(review)" v-bind="review" />
    </div>
  </section>
</template>

<script setup lang="ts">
import { reviews } from '../constants'
</script>

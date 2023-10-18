<template>
  <section class="flex justify-between items-center max-xl:flex-col-reverse gap-10 max-container">
    <div class="flex-1">
      <img
        :src="offer"
        alt="Shoe Promotion"
        width="773"
        height="687"
        class="object-contain w-full"
      />
    </div>
    <div class="flex flex-1 flex-col">
      <h2 class="text-4xl font-palanquin font-bold">
        <span class="text-coral-red">Special </span>
        Offer
      </h2>
      <p class="mt-4 info-text">
        Embark on a shopping journey that redefines your experience with unbeatable deals. From
        premier selections to incredible savings, we offer unparalleled value that sets us apart.
      </p>
      <p class="mt-6 info-text">
        Navigate a realm of possibilities designed to fulfill your unique desires, surpassing the
        loftiest expectations. Your journey with us is nothing short of exceptional.
      </p>
      <div class="mt-11 flex flex-wrap gap-4">
        <AppBtn label="Shop now" :iconURL="arrowRight" />
        <AppBtn
          label="Learn more"
          backgroundColor="bg-white"
          borderColor="border-slate-gray"
          textColor="text-slate-gray"
        />
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { arrowRight } from '../assets/icons'
import { offer } from '../assets/images'
</script>

<style scoped></style>

<script setup lang="ts"></script>

<template>
  <main className="relative">
    <GlobalNav />
    <section className="xl:padding-l wide:padding-r padding-b">
      <HomeHero />
    </section>
    <section className="padding">
      <PopularProducts />
    </section>
    <section className="padding">
      <SuperQuality />
    </section>
    <section className="padding-x py-10">
      <OurServices />
    </section>
    <section className="padding">
      <SpecialOffer />
    </section>
    <section className="bg-pale-blue padding">
      <CustomerReviews />
    </section>
    <section className="padding-x sm:py-32 py-16 w-full">
      <SubscribeUs />
    </section>
    <section className=" bg-black padding-x padding-t pb-8">
      <GlobalFooter />
    </section>
  </main>
</template>

<style scoped></style>

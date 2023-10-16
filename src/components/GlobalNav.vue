<template>
  <header class="padding-x py-8 absolute z-10 w-full">
    <nav class="flex justify-between items-center max-container">
      <a href="/">
        <img :src="headerLogo" alt="logo" width="129" height="29" class="m-0 w-[129px] h-[29px]" />
      </a>
      <ul
        class="flex-1 flex justify-center items-center gap-16 max-lg:hidden"
        v-for="item in navLinks"
        :key="item.label"
      >
        <li key="{item.label}">
          <a :href="item.href" class="font-montserrat leading-normal text-lg text-slate-gray">
            {{ item.label }}
          </a>
        </li>
      </ul>
      <div
        class="flex gap-2 text-lg leading-normal font-medium font-montserrat max-lg:hidden wide:mr-24"
      >
        <a href="/">Sign in</a>
        <span>/</span>
        <a href="/">Explore now</a>
      </div>
      <div class="hidden max-lg:block">
        <img :src="hamburger" alt="hamburger icon" width="25" height="25" />
      </div>
    </nav>
  </header>
</template>

<script setup lang="ts">
import { hamburger } from '@/assets/icons'
import { headerLogo } from '@/assets/images'
import { navLinks } from '@/constants'
</script>

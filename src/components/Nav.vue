<template>
  <header class="padding-x absolute z-10 w-full py-8">
    <nav class="max-container flex items-center justify-between">
      <a href="/">
        <img
          :src="headerLogo"
          alt="logo"
          width="129"
          height="29"
          class="m-0 h-[29px] w-[129px]"
        />
      </a>
      <ul class="flex flex-1 items-center justify-center gap-16 max-lg:hidden">
        <li v-for="item in navLinks" :key="item.label">
          <a
            :href="item.href"
            class="font-montserrat text-lg leading-normal text-slate-gray"
          >
            {{ item.label }}
          </a>
        </li>
      </ul>
      <div
        class="flex gap-2 font-montserrat text-lg font-medium leading-normal max-lg:hidden wide:mr-24"
      >
        <a href="/">Sign in</a>
        <span>/</span>
        <a href="/">Explore Now</a>
      </div>
      <div class="hidden max-lg:block">
        <img :src="hamburger" alt="hamburger icon" width="25" height="25" />
      </div>
    </nav>
  </header>
</template>

<script setup>
import { hamburger } from '../assets/icons'
import { headerLogo } from '../assets/images'
import { navLinks } from '../constants'

defineOptions({
  name: 'Nav',
})
</script>

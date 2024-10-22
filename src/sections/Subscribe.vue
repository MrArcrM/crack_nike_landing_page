<template>
  <section
    id="contact-us"
    class="max-container flex items-center justify-between gap-10 max-lg:flex-col"
  >
    <h3 class="font-palanquin text-4xl font-bold leading-[68px] lg:max-w-md">
      <div class="whitespace-nowrap">
        Sign Up for
        <span class="text-coral-red"> Updates </span>
      </div>
      & Newsletter
    </h3>
    <div
      class="flex w-full items-center gap-5 rounded-full p-2.5 max-sm:flex-col sm:border sm:border-slate-gray lg:max-w-[40%]"
    >
      <input type="text" placeholder="subscribe@nike.com" class="input" />
      <div>
        <Button label="Sign Up" fullWidth />
      </div>
    </div>
  </section>
</template>

<script setup>
import { Button } from '../components'

defineOptions({
  name: 'Subscribe',
})
</script>

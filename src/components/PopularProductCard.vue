<template>
  <div class="flex w-full flex-1 flex-col max-sm:w-full">
    <img :src="props.imgURL" :alt="props.name" class="h-[282px] w-[282px]" />
    <div class="mt-8 flex justify-start gap-2.5">
      <img :src="star" alt="rating icon" width="24" height="24" />
      <p class="font-montserrat text-xl leading-normal text-slate-gray">
        (4.5)
      </p>
    </div>
    <h3 class="mt-2 font-palanquin text-2xl font-semibold leading-normal">
      {{ props.name }}
    </h3>
    <p
      class="mt-2 font-montserrat text-2xl font-semibold leading-normal text-coral-red"
    >
      {{ props.price }}
    </p>
  </div>
</template>

<script setup>
import { star } from '../assets/icons'

const props = defineProps({
  imgURL: Object,
  name: String,
  price: String,
})
</script>

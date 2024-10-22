<template>
  <div class="flex flex-col items-center justify-center">
    <img
      :src="props.imgURL"
      alt="customer"
      class="h-[120px] w-[120px] rounded-full object-cover"
    />
    <p class="info-text mt-6 max-w-sm text-center">{{ props.feedback }}</p>
    <div class="mt-3 flex items-center justify-center gap-2.5">
      <img
        :src="star"
        alt="rating star"
        width="24"
        height="24"
        class="m-0 object-contain"
      />
      <p class="font-montserrat text-xl text-slate-gray">{{ props.rating }}</p>
    </div>
    <h3 class="mt-1 text-center font-palanquin text-3xl font-bold">
      {{ props.customerName }}
    </h3>
  </div>
</template>

<script setup>
import { star } from '../assets/icons'

const props = defineProps({
  imgURL: String,
  customerName: String,
  rating: Number,
  feedback: String,
})
</script>

<template>
  <section
    id="about-us"
    class="max-container flex w-full items-center justify-between gap-10 max-lg:flex-col"
  >
    <div class="flex flex-1 flex-col">
      <h2 class="font-palanquin text-4xl font-bold capitalize lg:max-w-lg">
        We Provide You
        <span class="text-coral-red"> Super </span>
        <span class="text-coral-red">Quality </span> Shoes
      </h2>
      <p class="info-text mt-4 lg:max-w-lg">
        Ensuring premium comfort and style, our meticulously crafted footwear is
        designed to elevate your experience, providing you with unmatched
        quality, innovation, and a touch of elegance.
      </p>
      <p class="info-text mt-6 lg:max-w-lg">
        Our dedication to detail and excellence ensures your satisfaction
      </p>
      <div class="mt-11">
        <Button label="View details" />
      </div>
    </div>

    <div>
      <img
        :src="shoe8"
        alt="product detail"
        width="570"
        height="522"
        class="object-contain"
      />
    </div>
  </section>
</template>
<script setup>
import { shoe8 } from '../assets/images'
import { Button } from '../components'
</script>

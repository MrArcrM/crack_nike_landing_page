<template>
  <section id="products" class="max-container max-sm:mt-12">
    <div class="flex flex-col justify-start gap-5">
      <h2 class="font-palanquin text-4xl font-bold">
        Our <span class="text-coral-red"> Popular </span> Products
      </h2>
      <p class="mt-2 font-montserrat text-slate-gray lg:max-w-lg">
        Experience top-notch quality and style with our sought-after selections.
        Discover a world of comfort, design, and value
      </p>
    </div>

    <div class="mt-16 grid lg:grid-cols-4 md:grid-cols-3 sm:grid-cols-2 grid-cols-1 sm:gap-6 gap-14">
      <PopularProductCard v-for="product in products" :key="product.name" v-bind="product" />
    </div>
  </section>
</template>
<script setup>
import {PopularProductCard} from '../components'
import {products} from '../constants'
</script>

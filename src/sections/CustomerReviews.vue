<template>
  <section class="max-container">
    <h3 class="text-center font-palanquin text-4xl font-bold">
      What Our
      <span class="text-coral-red"> Customers </span>Say?
    </h3>
    <p class="info-text m-auto mt-4 max-w-lg text-center">
      Hear genuine stories from our satisfied customers about their exceptional
      experiences with us.
    </p>

    <div
      class="mt-24 flex flex-1 items-center justify-evenly gap-14 max-lg:flex-col"
    >
      <ReviewCard
        v-for="(review, index) in reviews"
        :key="index"
        v-bind="review"
      />
    </div>
  </section>
</template>
<script setup>
import { ReviewCard } from '../components'
import { reviews } from '../constants'
</script>

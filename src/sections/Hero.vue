<template>
  <section
    id="home"
    class="max-container flex min-h-screen w-full flex-col justify-center gap-10 xl:flex-row"
  >
    <div
      class="max-xl:padding-x relative flex w-full flex-col items-start justify-center pt-28 xl:w-2/5"
    >
      <p class="font-montserrat text-xl text-coral-red">
        Our Summer collections
      </p>
      <h1
        class="mt-10 font-palanquin text-8xl font-bold max-sm:text-[72px] max-sm:leading-[82px]"
      >
        <span class="relative z-10 pr-10 xl:whitespace-nowrap xl:bg-white"
          >The New Arrival</span
        >
        <br />
        <span class="mt-3 inline-block text-coral-red">Nike</span> Shoes
      </h1>
      <p
        class="mb-14 mt-6 font-montserrat text-lg leading-8 text-slate-gray sm:max-w-sm"
      >
        Discover stylish Nike arrivals, quality comfort, and innovation for your
        active life.
      </p>

      <Button label="Shop Now" :iconURL="arrowRight" />

      <div class="mt-20 flex w-full flex-wrap items-start justify-start gap-16">
        <div v-for="(stat, index) in statistics" :key="index">
          <p class="font-palanquin text-4xl font-bold">{{ stat.value }}</p>
          <p class="font-montserrat leading-7 text-slate-gray">
            {{ stat.label }}
          </p>
        </div>
      </div>
    </div>

    <div
      class="bg-hero relative flex flex-1 items-center justify-center bg-primary bg-cover bg-center max-xl:py-40 xl:min-h-screen"
    >
      <img
        class="relative z-10 object-contain"
        :src="bigShoeImg"
        alt="shoe collection"
        width="610"
        height="502"
      />

      <div
        class="absolute -bottom-[5%] flex gap-4 max-sm:px-6 sm:left-[10%] sm:gap-6"
      >
        <div v-for="(image, index) in shoes" :key="index">
          <ShoeCard
            :index="index"
            :imgURL="image"
            :bigShoeImg="bigShoeImg"
            @changeBigShoeImage="setBigShoeImg"
          />
        </div>
      </div>
    </div>
  </section>
</template>
<script setup>
import { ref } from 'vue'
import { arrowRight } from '../assets/icons'
import { bigShoe1 } from '../assets/images'
import { Button, ShoeCard } from '../components'
import { shoes, statistics } from '../constants'

const bigShoeImg = ref(bigShoe1)

const setBigShoeImg = (shoe) => {
  bigShoeImg.value = shoe
}
</script>

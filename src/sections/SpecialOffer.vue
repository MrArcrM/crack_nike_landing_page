<template>
  <section
    class="max-container flex items-center justify-between gap-10 max-xl:flex-col-reverse"
  >
    <div class="flex-1">
      <img
        :src="offer"
        alt="Shoe Promotion"
        width="773"
        height="687"
        class="w-full object-contain"
      />
    </div>
    <div class="flex flex-1 flex-col">
      <h2 class="font-palanquin text-4xl font-bold">
        <span class="text-coral-red">Sepcial</span>
        Offer
      </h2>
      <p class="info-text mt-4">
        Embark on a shopping journey that redefines your experience with
        unbeatable deals. From premier selections to incredible savings, we
        offer unparalleled value that sets us apart.
      </p>
      <p class="info-text mt-6">
        Navigate a realm of possibilities designed to fulfill your unique
        desires, surpassing the loftiest expectations. Your journey with us is
        nothing short of exceptional.
      </p>
      <div class="mt-11 flex flex-wrap gap-4">
        <Button label="Shop now" :iconURL="arrowRight" />
        <Button
          label="Learn more"
          backgroundColor="bg-white"
          borderColor="border-slate-gray"
          textColor="text-slate-gray"
        />
      </div>
    </div>
  </section>
</template>
<script setup>
import { arrowRight } from '../assets/icons'
import { offer } from '../assets/images'
import { Button } from '../components'

defineOptions({
  name: 'SpecialOffer',
})
</script>

<template>
  <main class="relative">
    <Nav></Nav>
    <section class="xl:padding-l wide:padding-r padding-b">
      <Hero />
    </section>
    <section class="padding">
      <PopularProducts />
    </section>
    <section class="padding">
      <!-- <SuperQuality /> -->
    </section>
    <section class="padding-x py-10">
      <Services />
    </section>
    <section class="padding">
      <SpecialOffer />
    </section>
    <section class="padding bg-pale-blue">
      <CustomerReviews />
    </section>
    <section class="padding-x w-full py-16 sm:py-32">
      <Subscribe />
    </section>
    <section class="padding-x padding-t bg-black">Footer</section>
  </main>
</template>

<script setup>
import { Nav } from './components'
import {
  CustomerReviews,
  Hero,
  PopularProducts,
  Services,
  SpecialOffer,
  Subscribe,
} from './sections'
</script>

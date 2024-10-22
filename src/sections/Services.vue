<template>
  <section class="max-container flex justify-center flex-wrap gap-9">
    <ServiceCard v-for="service in services" :key="service.label" v-bind="service" />
  </section>
</template>
<script setup>
import { services } from '../constants';
import { ServiceCard } from '../components';
</script>

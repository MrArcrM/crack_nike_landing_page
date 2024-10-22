<template>
  <div
    class="w-full flex-1 rounded-[20px] px-10 py-16 shadow-3xl sm:w-[350px] sm:min-w-[350px]"
  >
    <div
      class="flex h-11 w-11 items-center justify-center rounded-full bg-coral-red"
    >
      <img :src="props.imgURL" :alt="props.label" width="24" height="24" />
    </div>
    <h3 class="mt-5 font-palanquin text-3xl font-bold leading-normal">
      {{ props.label }}
    </h3>
    <p
      class="mt-3 break-words font-montserrat text-lg leading-normal text-slate-gray"
    >
      {{ props.subtext }}
    </p>
  </div>
</template>
<script setup>
const props = defineProps({
  imgURL: String,
  label: String,
  subtext: String,
})

defineOptions({
  name: 'ServiceCard',
})
</script>

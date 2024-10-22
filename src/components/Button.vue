<template>
  <button :class="buttonClasses">
    {{ label }}
    <img
      v-if="iconURL"
      :src="iconURL"
      alt="arrow right icon"
      class="ml-2 h-5 w-5 rounded-full bg-white"
    />
  </button>
</template>
<script setup>
import { computed } from 'vue'

const props = defineProps({
  label: {
    type: String,
    required: true,
  },
  iconURL: {
    type: String,
    default: null,
  },
  backgroundColor: {
    type: String,
    default: null,
  },
  textColor: {
    type: String,
    default: null,
  },
  borderColor: {
    type: String,
    default: null,
  },
  fullWidth: {
    type: Boolean,
    default: false,
  },
})

const buttonClasses = computed(() => {
  return [
    'flex justify-center items-center gap-2 px-7 py-4 border font-montserrat text-lg leading-none rounded-full',
    props.backgroundColor
      ? `${props.backgroundColor} ${props.textColor} ${props.borderColor}`
      : 'bg-coral-red text-white border-coral-red',
    props.fullWidth ? 'w-full' : '',
  ].join(' ')
})

defineOptions({
  name: 'Button',
})
</script>

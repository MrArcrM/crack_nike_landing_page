<template>
  <div
    :class="[
      'cursor-pointer rounded-xl border-2 max-sm:flex-1',
      props.bigShoeImg === props.imgURL.bigShoe
        ? 'border-coral-red'
        : 'border-transparent',
    ]"
    @click="handleClick"
  >
    <div
      class="bg-card flex items-center justify-center rounded-xl bg-cover bg-center max-sm:p-4 sm:h-40 sm:w-40"
    >
      <img
        :src="props.imgURL.thumbnail"
        alt="shoe collection"
        width="127"
        height="103.34"
        class="object-contain"
      />
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  imgURL: Object,
  bigShoeImg: String,
})

const emit = defineEmits(['changeBigShoeImage'])

const handleClick = () => {
  if (props.bigShoeImg !== props.imgURL.bigShoe) {
    emit('changeBigShoeImage', props.imgURL.bigShoe)
  }
}
</script>

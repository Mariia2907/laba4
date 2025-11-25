<script setup lang="ts">
defineProps<{
  imageSrc: string
  title: string
  description: string
  activeStep: 1 | 2 | 3
}>()

const emit = defineEmits<{
  (e: 'next'): void
  (e: 'skip'): void
}>()
</script>

<template>
  <div class="w-full min-h-screen bg-white font-sans flex flex-col items-center justify-start px-5 pt-10 pb-10">

    <div class="w-full max-w-[350px] mt-10 mb-6">
      <img :src="imageSrc" :alt="title" class="w-full h-auto">
    </div>

    <h2 class="
      bg-[#FF5F5F]
      text-white
      text-[22px]
      font-semibold
      px-5 py-3
      rounded-md
      text-center
      mt-[50px] mb-[30px]
      max-w-full w-fit
    ">
      {{ title }}
    </h2>

    <p class="
      text-[#5A5A64]
      text-[12px]
      text-center
      leading-[1.6]
      max-w-[320px]
      mb-[70px]
      min-h-[130px]
    ">
      {{ description }}
    </p>

    <div class="w-full max-w-[350px] flex justify-between items-center mb-5">

      <button
        @click="emit('skip')"
        class="h-[34px] px-4 text-[12px] font-semibold rounded-md uppercase bg-[#F5F5FF] text-[#32323C]">
        Skip
      </button>

      <div class="flex gap-2 items-center">
        <span class="w-2 h-2 rounded-sm transition-colors duration-300" :class="activeStep === 1 ? 'bg-[#FF5F5F]' : 'bg-[#E8E8F5]'"></span>
        <span class="w-2 h-2 rounded-sm transition-colors duration-300" :class="activeStep === 2 ? 'bg-[#FF5F5F]' : 'bg-[#E8E8F5]'"></span>
        <span class="w-2 h-2 rounded-sm transition-colors duration-300" :class="activeStep === 3 ? 'bg-[#FF5F5F]' : 'bg-[#E8E8F5]'"></span>
      </div>

      <button
        @click="emit('next')"
        class="h-[34px] px-4 text-[12px] font-semibold rounded-md uppercase bg-[#FF6B6B] text-white">
        Next
      </button>
    </div>

  </div>
</template>

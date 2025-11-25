<script setup lang="ts">
import { useRouter } from 'vue-router'
import OnboardingCard from '@/components/OnboardingCard.vue'
import image1 from '@/assets/image.png'

const router = useRouter()

const handleNext = () => {
  router.push('/chat')
}

const handleSkip = () => {
  router.push('/chat')
}
</script>

<template>
  <OnboardingCard
    :imageSrc="image1"
    title="MEET NEW PEOPLE"
    description="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer lacinia tellus quis est pharetra fermentum. Curabitur dapibus neque id lacus hendrerit rhoncus. Vivamus quis pretium metus. Praesent varius tortor sit amet quam eleifend hendrerit. Vivamus pharetra ultrices diam vel volutpat. Praesent molestie lobortis sodales. Sed volutpat tempus orci."
    :activeStep="1"
    @next="handleNext"
    @skip="handleSkip"
  />
</template>

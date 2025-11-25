<script setup lang="ts">
import { useRouter } from 'vue-router'
import OnboardingCard from '@/components/OnboardingCard.vue'
import image2 from '@/assets/chat.png'

const router = useRouter()

const handleNext = () => {
  router.push('/')
}

const handleSkip = () => {
  router.push('/intro')
}
</script>

<template>
  <OnboardingCard
    :imageSrc="image2"
    title="CHAT WITH EASE"
    description="Maecenas in placerat nibh. Integer sollicitudin sapien et massa varius venenatis. Nulla facilisis purus nec nibh posuere volutpat. Nunc congue, arcu sit amet imperdiet sodales, tellus odio sagittis turpis, sed tincidunt nibh urna in leo. Duis et sodales elit, ut cursus est. Aenean magna metus, volutpat vel dignissim quis, malesuada eget ex."
    :activeStep="2"
    @next="handleNext"
    @skip="handleSkip"
  />
</template>

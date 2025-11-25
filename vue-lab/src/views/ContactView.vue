<script setup lang="ts">
import UserCard from '@/components/UserCard.vue';
</script>

<template>
  <div class="contact-page">
    <h1>Сторінка контактів</h1>
    <p>Це наша нова сторінка контактів!</p>
    <UserCard username="Student_1" :isActive="5432" />
    <UserCard username="Student_2" :isActive="false" />
  </div>
</template>
/*Type 'number' is not assignable to type 'boolean'.(Помилка виникає через те,що ми передаємо часло замість буліана)*/

<style scoped>
/* Стилі <style scoped> застосовуються лише до цього компонента */
.contact-page {
  padding: 20px;
}
</style>

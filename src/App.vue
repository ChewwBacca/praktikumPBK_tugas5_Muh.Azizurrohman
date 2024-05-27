<template>
  <q-layout view="hHh lpR fFf">
    <!-- Navbar -->
    <Navbar />

    <!-- Main Content -->
    <q-page-container>
      <q-page class="q-pa-md">
        <!-- Carousel -->
        <Carousel />

        <!-- Cards -->
        <CardList />
      </q-page>
    </q-page-container>

    <!-- Footer -->
    <Footer />
  </q-layout>
</template>

<script setup>
// Gunakan jalur relatif untuk impor komponen
import Navbar from './components/Navbar.vue';
import Carousel from './components/Carousel.vue';
import CardList from './components/CardList.vue';
import Footer from './components/Footer.vue';
</script>

<style scoped>
</style>

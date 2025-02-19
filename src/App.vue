<script setup>
import Header from './components/Header.vue';
import Slider from './components/Slider.vue';
import CardInvest from './components/CardInvest.vue';
import CardManager from './components/CardManager.vue';
import Footer from './components/Footer.vue';
</script>

<template>
  <Header />
  <main class="container mx-auto">
    <Slider />
    <div>
      <h2 class="mx-[24px] md:mx-auto text-[22px] md:text-[36px] mb-[40px] text-[#0048CE]">Инвестиционный отдел</h2>
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 justify-center gap-[40px] mx-[24px] md:mx-auto mb-[40px] md:mb-[60px]">
        <CardInvest />
      </div>
    </div>
    <div>
      <h2 class="mx-[24px] md:mx-auto text-[22px] md:text-[36px] mb-[40px] text-[#0048CE]">Маркетинг</h2>
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 justify-center gap-[40px] mx-[24px] md:mx-auto mb-[40px] md:mb-[60px]">
        <CardManager />
      </div>
    </div>
  </main>
  <Footer />
</template>
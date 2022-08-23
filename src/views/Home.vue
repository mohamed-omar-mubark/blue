<template>
  <div class="home">
    <benefits></benefits>
    <offers></offers>
  </div>
</template>

<script>
  export default {
    name: 'Home',
    components: {
      benefits: () => import('@/components/pages/home/Benefits.vue'),
      offers: () => import('@/components/pages/home/Offers.vue')
    }
  }
</script>

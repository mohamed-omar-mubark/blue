<template>
  <div class="home">
    <benefits></benefits>
    <offers></offers>
    <ourAgents></ourAgents>
  </div>
</template>

<script>
  export default {
    name: 'Home',
    components: {
      benefits: () => import('@/components/pages/home/Benefits.vue'),
      offers: () => import('@/components/pages/home/Offers.vue'),
      ourAgents: () => import('@/components/pages/home/OurAgents.vue')
    }
  }
</script>

<template>
  <div class="home">
    <benefits></benefits>
    <offers></offers>
    <modernLayouts></modernLayouts>
    <ourAgents></ourAgents>
    <testimonials></testimonials>
    <sponsors></sponsors>
    <appFooter></appFooter>
  </div>
</template>

<script>
  export default {
    name: 'Home',
    components: {
      benefits: () => import('@/components/pages/home/Benefits.vue'),
      offers: () => import('@/components/pages/home/Offers.vue'),
      modernLayouts: () => import('@/components/pages/home/ModernLayouts.vue'),
      ourAgents: () => import('@/components/pages/home/OurAgents.vue'),
      testimonials: () => import('@/components/pages/home/Testimonials.vue'),
      sponsors: () => import('@/components/pages/home/Sponsors.vue'),
      appFooter: () => import('@/layouts/global/Footer.vue')
    }
  }
</script>

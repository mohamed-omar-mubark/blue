<template>
  <div class="home">
    <banner></banner>
    <benefits></benefits>
    <featured></featured>
    <offers></offers>
    <modernLayouts></modernLayouts>
    <customForm></customForm>
    <contentTypes></contentTypes>
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
      banner: () => import('@/components/pages/home/Banner.vue'),
      benefits: () => import('@/components/pages/home/Benefits.vue'),
      featured: () => import('@/components/pages/home/Featured.vue'),
      offers: () => import('@/components/pages/home/Offers.vue'),
      modernLayouts: () => import('@/components/pages/home/ModernLayouts.vue'),
      customForm: () => import('@/components/pages/home/CustomForm.vue'),
      ourAgents: () => import('@/components/pages/home/OurAgents.vue'),
      contentTypes: () => import('@/components/pages/home/ContentTypes.vue'),
      testimonials: () => import('@/components/pages/home/Testimonials.vue'),
      sponsors: () => import('@/components/pages/home/Sponsors.vue'),
      appFooter: () => import('@/layouts/global/Footer.vue')
    }
  }
</script>

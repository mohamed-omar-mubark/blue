<template>
  <div class="home">
    <benefits></benefits>
  </div>
</template>

<script>
  export default {
    name: 'Home',
    components: {
      benefits: () => import('@/components/pages/home/Benefits.vue')
    }
  }
</script>

<template>
  <div class="home">
    <carousel></carousel>
  </div>
</template>

<script>
  export default {
    name: 'Home',
    components: {
      carousel: () => import('@/components/pages/home/Carousel.vue')
    }
  }
</script>

<template>
  <section class='carousel'>
    <v-carousel
      :show-arrows="false"
      hide-delimiters
      cycle
      interval="5000"
    >
      <v-carousel-item
        src="@/assets/images/pages/home/carousel/chicago.jpg"
      ></v-carousel-item>

      <v-carousel-item
        src="@/assets/images/pages/home/carousel/new-york.jpg"
      ></v-carousel-item>

      <v-carousel-item
        src="@/assets/images/pages/home/carousel/miami-beach.jpg"
      ></v-carousel-item>
    </v-carousel>
  </section>
</template>

<script>
  export default {
    name: 'Carousel',
  };
</script>

<style lang='scss' scoped>

</style>
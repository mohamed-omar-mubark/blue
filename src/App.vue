<template>
  <v-app>
    <v-main>
      <!-- preloading -->
      <Loading />
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>
  import Loading from '@/components/loading/Loading.vue'
  export default {
    name: 'App',
    components: {
      Loading
    },
  };
</script>

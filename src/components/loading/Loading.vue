<template>
  <section class='loading' v-if="show">
    <h1>BLUE</h1>
  </section>
</template>

<script>
  export default {
    name: 'Loading',
    data() {
      return {
        show: true
      };
    },
    mounted() {
      this.toggleLoading();
    },
    methods: {
      // toggleLoading
      toggleLoading() {
        setTimeout(() => {
          this.show = false;
        }, 2000);
      }
    }
  };
</script>

<style lang='scss' scoped>
  .loading {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: #fff;
    z-index: 9999;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    
    h1 {
      font-size: 3rem;
      color: var(--info-color);
      animation: loading 2s linear infinite;
    }

    @keyframes loading {
      0% {
        opacity: 0;
      }
      100% {
        opacity: 1;
      }
    }
  }
</style>
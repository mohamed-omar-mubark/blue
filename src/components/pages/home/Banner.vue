<template>
  <section class='banner'>
    <div class="content">
      <span class="main-title d-block">Welcome to BLUE</span>
      <p class="paragraph">
        Packed with 100+ new features and improvements, it is the biggest <br> all-in-one solution for real estate companies and professionals
      </p>
    </div>
  </section>
</template>

<script>
  export default {
    name: 'Banner',
    mounted() {
      this.durationSlider()
    },
    methods: {
      durationSlider() {
        let banner = document.querySelector('.banner')
        var listItems = 2;
        var count = 0;
        
        setInterval(() => {
          banner.style.backgroundImage = "url('https://default.houzez.co/wp-content/uploads/2016/03/new-york.jpg')";
          console.log(count);

          count += 1;
          if (count >= listItems) {
            banner.style.backgroundImage = "url('https://default.houzez.co/wp-content/uploads/2020/03/miami-beach.jpg')";
            count = 0;
          }
        }, 5000);
      }
    }
  };
</script>

<style lang='scss' scoped>
  .banner {
    position: relative;
    height: 620px;
    background-image: url('https://default.houzez.co/wp-content/uploads/2020/03/miami-beach.jpg');
    background-position: 50%;
    background-size: 100%;
    animation: bannerBg 5s infinite;
    transition: .2s;
    @media (max-width: 992px) {
      background-size: cover;
    }
    
    .content {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      padding: 20px;
      background-color: transparent;
      background-image: linear-gradient(180deg, rgba(0, 66, 116, 0.35) 0%, #004274 100%);
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;

      .main-title {
        text-align: center;
        font-size: 2.8125rem;
        font-weight: 300;
        color: var(--white-color);
        margin-bottom: 10px;
      }

      .paragraph {
        text-align: center;
        font-size: 1.5625rem;
        font-weight: 300;
        color: var(--white-color);
        line-height: 1.5em;
      }
    }
  }
  @media (min-width: 992px) {
    @keyframes bannerBg {
      0% {
        background-size: 100%;
      }
      50% {
        background-size: 105%;
      }
      100% {
        background-size: 100%;
      }
    }
  }
</style>
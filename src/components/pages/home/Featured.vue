<template>
  <section class='featured'>
    <v-container>
      <div class="head">
        <span class="section-title">Display Latest & Featured Properties</span>
        <p class="paragraph">
          With the features and filters provided with the Blue widgets you can turn your visitors attention to <br> the latest listings or the ones that are most profitable to buy at the moment.
        </p>
      </div>

      <carousel :items="3" :margin="30" :loop="true" :nav="false" :dots="false" :autoplay="true" :autoplayHoverPause="true" :responsive="{0:{items:1},767:{items:2},992:{items:3},1200:{items:4}}">
        <div class="carousel-item">
          <div class="image">
            <div class="bg">
              <span class="type">Featured</span>
              <span class="price">$240,000</span>
            </div>
            <img src="https://432351-1355208-raikfcquaxqncofqfm.stackpathdns.com/wp-content/uploads/2016/02/038-592x444.jpg">
          </div>
          <div class="text-content">
            <span class="item-name d-block">Modern apartment on the bay</span>
            <div class="item-details">
              <div class="detail-box">
                <v-icon>bed</v-icon>
                <span class="value">4</span>
              </div>
              <div class="detail-box">
                <v-icon>bathtub</v-icon>
                <span class="value">2</span>
              </div>
              <div class="detail-box">
                <v-icon>square_foot</v-icon>
                <span class="value">1200 Sq Ft</span>
              </div>
            </div>
            <span class="subtitle">Apartment</span>
          </div>
        </div>
        <div class="carousel-item">
          <div class="image">
            <div class="bg">
              <span class="type">Featured</span>
              <span class="price">$850,000</span>
            </div>
            <img src="https://432351-1355208-raikfcquaxqncofqfm.stackpathdns.com/wp-content/uploads/2016/03/043-592x444.jpg">
          </div>
          <div class="text-content">
            <span class="item-name d-block">Awesome family home</span>
            <div class="item-details">
              <div class="detail-box">
                <v-icon>bed</v-icon>
                <span class="value">4</span>
              </div>
              <div class="detail-box">
                <v-icon>bathtub</v-icon>
                <span class="value">2</span>
              </div>
              <div class="detail-box">
                <v-icon>square_foot</v-icon>
                <span class="value">1200 Sq Ft</span>
              </div>
            </div>
            <span class="subtitle">Home</span>
          </div>
        </div>
        <div class="carousel-item">
          <div class="image">
            <div class="bg">
              <span class="type">Featured</span>
              <span class="price">$50,000</span>
            </div>
            <img src="https://432351-1355208-raikfcquaxqncofqfm.stackpathdns.com/wp-content/uploads/2016/03/026-592x444.jpg">
          </div>
          <div class="text-content">
            <span class="item-name d-block">Renovated studio</span>
            <div class="item-details">
              <div class="detail-box">
                <v-icon>bed</v-icon>
                <span class="value">4</span>
              </div>
              <div class="detail-box">
                <v-icon>bathtub</v-icon>
                <span class="value">2</span>
              </div>
              <div class="detail-box">
                <v-icon>square_foot</v-icon>
                <span class="value">1200 Sq Ft</span>
              </div>
            </div>
            <span class="subtitle">Studio</span>
          </div>
        </div>
        <div class="carousel-item">
          <div class="image">
            <div class="bg">
              <span class="type">Featured</span>
              <span class="price">$80,000</span>
            </div>
            <img src="https://432351-1355208-raikfcquaxqncofqfm.stackpathdns.com/wp-content/uploads/2016/03/019-592x444.jpg">
          </div>
          <div class="text-content">
            <span class="item-name d-block">Penthouse apartment</span>
            <div class="item-details">
              <div class="detail-box">
                <v-icon>bed</v-icon>
                <span class="value">4</span>
              </div>
              <div class="detail-box">
                <v-icon>bathtub</v-icon>
                <span class="value">2</span>
              </div>
              <div class="detail-box">
                <v-icon>square_foot</v-icon>
                <span class="value">1200 Sq Ft</span>
              </div>
            </div>
            <span class="subtitle">Apartment</span>
          </div>
        </div>
      </carousel>
    </v-container>
  </section>
</template>

<script>
  import carousel from 'vue-owl-carousel'

  export default {
    name: 'Featured',
    components: {
      carousel
    }
  };
</script>

<style lang='scss' scoped>
  .featured {
    padding: 100px 0;

    .head {
      text-align: center;
      margin-bottom: 40px;
      
      .section-title {
        font-size: 2.1875rem;
        font-weight: 400;
        color: var(--dark-color);
        margin-bottom: 10px;
      }
      .paragraph {
        font-size: 1.125rem;
        font-weight: 300;
        color: var(--secondary-color);
        margin-bottom: 16px;
      }
    }

    .carousel-item {
      &:hover {
        .image {
          .bg {
            background-color: rgba(0, 0, 0, .1);
          }
        }
      }

      .image {
        position: relative;
        border-radius: 4px;
        overflow: hidden;
        margin-bottom: 20px;

        .bg {
          position: absolute;
          display: flex;
          flex-direction: column;
          justify-content: space-between;
          align-items: flex-start;
          top: 0;
          left: 0;
          width: 100%;
          height: 100%;
          padding: 30px;
          background-color: rgba(0, 0, 0, .3);
          transition: 0.3s;

          .type {
            padding: 2px 10px;
            background-color: #61ce70;
            border-radius: 4px;
            font-size: .75rem;
            font-weight: 300;
            color: var(--white-color);
          }

          .price {
            font-size: 1rem;
            font-weight: 600;
            color: var(--white-color);
          }
        }
      }
      
      .text-content {
        text-align: center;

        .item-name {
          font-size: 1rem;
          font-weight: 500;
          color: var(--dark-color);
          margin-bottom: 5px;
        }

        .item-details {
          display: flex;
          justify-content: center;
          align-items: center;
          gap: 10px;

          .detail-box {
            display: flex;
            justify-content: start;
            align-items: center;
            gap: 5px;

            * {
              color: var(--secondary-color);
            }

            .v-icon {
              font-size: 1.2rem;
            }

            .value {
              font-size: .8125rem;
              font-weight: 300;
            }
          }
        }

        .subtitle {
          font-size: .75rem;
          font-weight: 400;
          color: var(--dark-color);
        }
      }
    }
  }
</style>
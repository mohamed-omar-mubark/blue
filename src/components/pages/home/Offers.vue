<template>
  <section class='offers'>
    <v-container>
      <div class="overlay"></div>
      <div class="content">
        <span class="section-title d-block">
          Blue offers a wide range of drag-and-drop widgets
          <br>
          to assist you in designing your pages
        </span>

        <div class="cards">
          <v-card
            v-for="card in cards"
            :key="card.id"
            flat
            class="text-center"
          >
            <v-icon>{{ card.icon }}</v-icon>
            <router-link :to="card.href">{{ card.text }}</router-link>
          </v-card>
        </div>
      </div>
    </v-container>
  </section>
</template>

<script>
  export default {
    name: 'Offers',
    data() {
      return {
        cards: [
          {
            id: 1,
            icon: 'price_check',
            text: 'Looking to buy',
            href: '#'
          },
          {
            id: 2,
            icon: 'sell',
            text: 'Sell your home',
            href: '#'
          },
          {
            id: 3,
            icon: 'real_estate_agent',
            text: 'Rent a place',
            href: '#'
          },
          {
            id: 4,
            icon: 'info',
            text: 'Need help?',
            href: '#'
          }
        ]
      }
    }
  };
</script>

<style lang='scss' scoped>
  .offers {
    display: flex;
    justify-content: center;
    align-items: center;
    position: relative;
    padding: 100px 0;
    min-height: 750px;
    background-image: url('https://default.houzez.co/wp-content/uploads/2020/03/205.jpg');
    background-position: center center;
    background-repeat: no-repeat;
    background-size: cover;
    background-attachment: fixed;
    &::before {
      position: absolute;
      content: '';
      top: 0;
      left: 0;
      width: 100%;
      height: 100px;
      z-index: 1;
      background-image: linear-gradient(178deg, var(--white-color) 50%, transparent calc(50% + 2px));
      @media (max-width: 575px) {
        height: 40px;
      }
    }
    &::after {
      position: absolute;
      content: '';
      bottom: 0;
      left: 0;
      width: 100%;
      height: 100px;
      background-image: linear-gradient(178deg, transparent 50%, var(--white-color) calc(50% + 2px));
      @media (max-width: 575px) {
        height: 40px;
      }
    }

    .overlay {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 66, 116, 0.45);
      opacity: 1;
    }

    .content {
      position: relative;
      .section-title {
        font-size: 1.875rem;
        font-weight: 300;
        color: var(--white-color);
        text-align: center;
        line-height: 1.35em;
        margin-bottom: 40px;
      }

      .cards {
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 1px;
        flex-wrap: wrap;

        .v-card {
          background-color: rgba(0, 66, 116, 0.71);
          padding: 30px;
          border-radius: 0;
          min-width: 230px;
          min-height: 150px;
          transition: 0.3s;
          &:hover {
            box-shadow: 0 70px 70px rgba(0, 0, 0, .2) !important;
            -webkit-transform: translate(0,-10px);
            -ms-transform: translate(0,-10px);
            transform: translate(0,-10px);
          }

          .v-icon {
            display: block;
            margin-bottom: 15px;
            font-size: 40px;
            color: var(--white-color);
          }

          a {
            font-size: 1rem;
            font-weight: 300;
            color: var(--white-color);
          }
        }
      }
    }
  }
</style>
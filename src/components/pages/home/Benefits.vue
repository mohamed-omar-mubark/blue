<template>
  <section class='benefits'>
    <v-container>
      <div class="cards">
        <v-card
          v-for="card in cards"
          :key="card.id"
          flat
          class="text-center"
        >
          <span class="card-title">{{ card.title }}</span>
          <p class="paragraph">
            {{ card.content }}
          </p>
          <router-link :to="card.href">{{ card.link_text }}</router-link>
        </v-card>
      </div>
    </v-container>
  </section>
</template>

<script>
  export default {
    name: 'Benefits',
    data() {
      return {
        cards: [
          {
            id: 1,
            title: 'Easy to get started',
            content: 'Get ready to launch your realty site in minutes without any previous experience',
            link_text: 'Learn more',
            href: '#'
          },
          {
            id: 2,
            title: 'Highly customizable',
            content: 'Customize the site to your expectations by using all of the theme features',
            link_text: 'Learn more',
            href: '#'
          },
          {
            id: 3,
            title: 'Drag-and-drop based',
            content: 'Design your page by simply dragging the features using Elementor page builder',
            link_text: 'Learn more',
            href: '#'
          }
        ]
      }
    }
  };
</script>

<style lang='scss' scoped>
  .benefits {
    position: relative;
    padding: 30px 20px 90px;
    min-height: 500px;
    background-color: var(--main-color);
    overflow: hidden;
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

    .cards {
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 1px;
      @media (max-width: 1264px) {
        flex-wrap: wrap;
      }

      .v-card {
        background-color: transparent;
        background-image: linear-gradient(180deg, rgba(255, 255, 255, 0.1) 0%, rgba(242, 41, 91, 0) 100%);
        padding: 35px;
        border-radius: 0;
        min-height: 250px;
        transition: 0.3s;
        &:hover {
          box-shadow: 0 70px 70px rgba(0, 0, 0, .2) !important;
          -webkit-transform: translate(0,-10px);
          -ms-transform: translate(0,-10px);
          transform: translate(0,-10px);
        }

        .card-title {
          font-size: 1.125rem;
          font-weight: 400;
          color: var(--white-color);
        }

        .paragraph {
          padding: 10px 0 20px;
          font-size: 1.0625rem;
          font-weight: 300;
          line-height: 1.5em;
          color: var(--white-color);
          max-width: 360px;
          margin: 0 auto;
        }

        a {
          font-size: 1rem;
          font-weight: 500;
          color: var(--info-color);
        }
      }
    }
  }
</style>
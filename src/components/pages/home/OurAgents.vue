<template>
  <section class='our-agents text-center'>
    <v-container>
      <div class="head">
        <span class="section-title">Meet Our Agents</span>
        <p class="paragraph">
          Lorem ipsum dolor sit amet, consectetur adipisicing elit
        </p>
      </div>

      <div class="cards">
        <v-card
          v-for="card in cards"
          :key="card.id"
          flat
          class="text-center"
        >
          <v-img
            :src="card.image"
            :alt="card.title"
            max-width="150"
            max-height="150"
            class="rounded-circle"
          ></v-img>
          <span class="card-title">{{ card.title }}</span>
        </v-card>
      </div>
    </v-container>
  </section>
</template>

<script>
  export default {
    name: 'OurAgents',
    data() {
      return {
        cards: [
          {
            id: 1,
            image: 'https://432351-1355208-raikfcquaxqncofqfm.stackpathdns.com/wp-content/uploads/2016/02/agent-3-150x150.jpg',
            title: 'Samuel Palmer',
            subtitle: 'Company Agent , Modern House Real Estate',
            description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus porta justo eget risus consectetur,...',
            link_text: 'view Profile',
            href: '#'
          },
          {
            id: 2,
            image: 'https://432351-1355208-raikfcquaxqncofqfm.stackpathdns.com/wp-content/uploads/2016/02/agent-4-150x150.jpg',
            title: 'Vincent Fuller',
            subtitle: 'Company Agent , Country House Real Estate',
            description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus porta justo eget risus consectetur,...',
            link_text: 'view Profile',
            href: '#'
          },
          {
            id: 3,
            image: 'https://432351-1355208-raikfcquaxqncofqfm.stackpathdns.com/wp-content/uploads/2016/02/Artboard-2team-150x150.jpg',
            title: 'Brittany Watkins',
            subtitle: 'Company Agent , All American Real Estate',
            description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus porta justo eget risus consectetur,...',
            link_text: 'view Profile',
            href: '#'
          },
          {
            id: 4,
            image: 'https://432351-1355208-raikfcquaxqncofqfm.stackpathdns.com/wp-content/uploads/2016/02/agent-1-150x150.jpg',
            title: 'Michelle Ramirez',
            subtitle: 'Company Agent , Modern House Real Estate',
            description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus porta justo eget risus consectetur,...',
            link_text: 'view Profile',
            href: '#'
          }
        ]
      }
    }
  };
</script>

<style lang='scss' scoped>
  .our-agents {
    padding: 100px 0;

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

    .cards {
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 1px;
      flex-wrap: wrap;

      .v-card {
        padding: 35px;
        border-radius: 0;
        min-height: 480px;
        transition: 0.3s;
        &:hover {
          box-shadow: 0 70px 70px rgba(0, 0, 0, .2) !important;
          -webkit-transform: translate(0,-10px);
          -ms-transform: translate(0,-10px);
          transform: translate(0,-10px);
        }
        
        .v-image {
          margin-bottom: 30px;
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
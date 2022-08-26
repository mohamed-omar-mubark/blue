<template>
  <section class='testimonials'>
    <v-container>
      <div class="head">
        <span class="section-title">Testimonials</span>
        <p class="paragraph">
          Lorem ipsum dolor sit amet, consectetur adipisicing elit
        </p>
      </div>

      <div class="cards">
        <v-card
          v-for="card in cards"
          :key="card.id"
          flat
        >
          <v-icon>format_quote</v-icon>
          <p class="paragraph">
            {{ card.content }}
          </p>
          <div class="author">
            <img :src="card.author.image" :alt="card.author.name">
            <div class="text">
              <span class="name d-block">by <span>{{ card.author.name }}</span></span>
              <span class="author-title">{{ card.author.title }}</span>
            </div>
          </div>
        </v-card>
      </div>
    </v-container>
  </section>
</template>

<script>
  export default {
    name: 'Testimonials',
    data() {
      return {
        cards: [
          {
            id: 1,
            content: "Really good Theme. We can't understand how we've been living without Blue.",
            author: {
              image: 'https://432351-1355208-raikfcquaxqncofqfm.stackpathdns.com/wp-content/uploads/2016/03/128.jpg',
              name: 'Roy Bennett',
              title: 'Marketing Manager, Envato'
            }
          },
          {
            id: 2,
            content: 'Great work on your Blue. I like it more and more each day because it makes my life easier and lot profitable.',
            author: {
              image: 'https://432351-1355208-raikfcquaxqncofqfm.stackpathdns.com/wp-content/uploads/2016/03/128-2.jpg',
              name: 'Kenneth Sandoval',
              title: 'Realtor, Envato'
            }
          },
          {
            id: 3,
            content: 'Blue is the next killer theme. I strongly recommend Blue to everyone interested in running a successful online business!',
            author: {
              image: 'https://432351-1355208-raikfcquaxqncofqfm.stackpathdns.com/wp-content/uploads/2016/03/128-3.jpg',
              name: 'Kathleen Peterson',
              title: 'Sales Manager, Envato'
            }
          }
        ]
      }
    }
  };
</script>

<style lang='scss' scoped>
  .testimonials {
    padding: 100px 0;

    .head {
      text-align: center;
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

    .cards {
      display: flex;
      justify-content: center;
      align-items: flex-start;
      gap: 1px;
      @media (max-width: 992px) {
        flex-wrap: wrap;
      }

      .v-card {
        padding: 40px;
        width: 325px;

        .v-icon {
          font-size: 2rem;
        }

        .paragraph {
          margin: 10px 0 30px;
          font-size: 0.9375rem;
          font-weight: 300;
          line-height: 1.5em;
          color: var(--secondary-color);
          max-width: 270px;
        }

        .author {
          display: flex;
          justify-content: start;
          align-items: flex-start;
          gap: 20px;

          img {
            width: 75px;
            height: 75px;
            border-radius: 50%;
            object-fit: cover;
            object-position: center;
          }

          .text {
            .name {
              font-size: 0.9375rem;
              font-weight: 300;
              color: var(--secondary-color);
              width: max-content;

              span {
                font-size: 0.9375rem;
                font-weight: 500;
                color: var(--dark-color);
              }

              .author-title {
                font-size: 1rem;
                font-weight: 300;
                color: var(--secondary-color);
              }
            }
          }
        }
      }
    }
  }
</style>
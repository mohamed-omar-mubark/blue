<template>
  <section class='sponsors'>
    <div class="cards">
      <v-card
        v-for="card in cards"
        :key="card.id"
        flat
      >
        <img :src="card.image">
      </v-card>
    </div>
  </section>
</template>

<script>
  export default {
    name: 'Sponsors',
    data() {
      return {
        cards: [
          {
            id: 1,
            image: 'https://432351-1355208-raikfcquaxqncofqfm.stackpathdns.com/wp-content/uploads/2020/03/partner-01-e1582734705113.jpg'
          },
          {
            id: 2,
            image: 'https://432351-1355208-raikfcquaxqncofqfm.stackpathdns.com/wp-content/uploads/2020/03/partner-02-e1582734691936.jpg'
          },
          {
            id: 3,
            image: 'https://432351-1355208-raikfcquaxqncofqfm.stackpathdns.com/wp-content/uploads/2020/03/partner-04-e1582734649458.jpg'
          },
          {
            id: 4,
            image: 'https://432351-1355208-raikfcquaxqncofqfm.stackpathdns.com/wp-content/uploads/2020/03/partner-03-e1582734671602.jpg'
          },
          {
            id: 5,
            image: 'https://432351-1355208-raikfcquaxqncofqfm.stackpathdns.com/wp-content/uploads/2020/03/partner-05-e1582734603812.jpg'
          },
        ]
      }
    }
  };
</script>

<style lang='scss' scoped>
  .sponsors {
    padding: 15px 0;
    border-top: 1px solid #ECECEC;

    .cards {
      display: flex;
      justify-content: center;
      align-items: flex-start;
      gap: 10px;
      flex-wrap: wrap;

      .v-card {
        padding: 10px;
        width: max-content;
        @media (max-width: 1120px) {
          margin-bottom: 20px;
        }

        img {
          width: auto;
          height: 60px;
          object-fit: cover;
          object-position: center;
        }
      }
    }
  }
</style>
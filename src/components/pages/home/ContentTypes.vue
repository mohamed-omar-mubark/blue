<template>
  <section class='content-types'>
    <v-container>
      <div class="head">
        <span class="section-title">Display Different Content Types</span>
        <p class="paragraph">
          The Blue Grids widgets allow you to display property cities, types, status, etc within different grid <br> style variations, colors and typography options
        </p>
      </div>

      <div class="columns">
        <div class="column column-1">
          <v-card
            flat
            class="card-1"
          >
            <span class="main-title">Apartment</span>
            <span class="subtitle">17 Properties</span>
          </v-card>

          <div class="double-card">
            <v-card
              flat
              class="card-2"
            >
              <span class="main-title">Studio</span>
              <span class="subtitle">7 Properties</span>
            </v-card>

            <v-card
              flat
              class="card-3"
            >
              <span class="main-title">Shop</span>
              <span class="subtitle">3 Properties</span>
            </v-card>
          </div>

          <v-card
            flat
            class="card-4"
          >
            <span class="main-title">Condo</span>
            <span class="subtitle">5 Properties</span>
          </v-card>
        </div>

        <div class="column column-2">
          <div class="double-card">
            <v-card
              flat
              class="card-5"
            >
              <span class="main-title">Villa</span>
              <span class="subtitle">10 Properties</span>
            </v-card>

            <v-card
              flat
              class="card-6"
            >
              <span class="main-title">Single Family Home</span>
              <span class="subtitle">10 Properties</span>
            </v-card>
          </div>

          <v-card
            flat
            class="card-7"
          >
            <span class="main-title">Office</span>
            <span class="subtitle">3 Properties</span>
          </v-card>

          <div class="double-card">
            <v-card
              flat
              class="card-8"
            >
              <span class="main-title">Lot</span>
              <span class="subtitle">6 Properties</span>
            </v-card>

            <v-card
              flat
              class="card-9"
            >
              <span class="main-title">Multi Family Home</span>
              <span class="subtitle">9 Properties</span>
            </v-card>
          </div>
        </div>
      </div>
    </v-container>
  </section>
</template>

<script>
  export default {
    name: 'ContentTypes',
  };
</script>

<style lang='scss' scoped>
  .content-types {
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

    .columns {
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 30px;
      @media (max-width: 1200px) {
        flex-wrap: wrap;
      }

      .column {
        width: 545px;
        @media (max-width: 575px) {
          width: 100%;
        }

        // global
        .v-card {
          display: flex;
          flex-direction: column;
          justify-content: center;
          align-items: center;
          position: relative;
          padding: 30px;
          border-radius: 4px;
          overflow: hidden;
          background-size: cover;
          background-repeat: no-repeat;
          background-position: center;
          width: 100%;

          &::before {
            position: absolute;
            content: '';
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, .3);
            transition: 0.3s;
          }

          &:hover {
            &::before {
              background-color: rgba(0, 0, 0, .1);
            }
          }

          .main-title {
            position: relative;
            font-size: 1.25rem;
            font-weight: 400;
            color: var(--white-color);
          }

          .subtitle {
            position: relative;
            font-size: .75rem;
            font-weight: 300;
            color: var(--white-color);
          }

          &.card-1 {
            background-image: url('https://432351-1355208-raikfcquaxqncofqfm.stackpathdns.com/wp-content/uploads/2020/03/205.jpg');
            height: 258px;
            margin-bottom: 30px;
          }

          &.card-4 {
            background-image: url('https://432351-1355208-raikfcquaxqncofqfm.stackpathdns.com/wp-content/uploads/2016/02/039.jpg');
            height: 258px;
          }

          &.card-7 {
            background-image: url('https://432351-1355208-raikfcquaxqncofqfm.stackpathdns.com/wp-content/uploads/2016/03/206.jpg');
            height: 258px;
            margin-bottom: 30px;
          }
        }

        .double-card {
          display: flex;
          justify-content: space-between;
          align-items: center;
          gap: 30px;
          @media (max-width: 575px) {
            flex-wrap: wrap;
          }
          &:not(:last-of-type) {
            margin-bottom: 30px;
          }
            
          .card-2 {
            background-image: url('https://432351-1355208-raikfcquaxqncofqfm.stackpathdns.com/wp-content/uploads/2016/03/023.jpg');
            height: 257px;
          }
          .card-3 {
            background-image: url('https://432351-1355208-raikfcquaxqncofqfm.stackpathdns.com/wp-content/uploads/2016/03/203.jpg');
            height: 257px;
          }

          .card-5 {
            background-image: url('https://432351-1355208-raikfcquaxqncofqfm.stackpathdns.com/wp-content/uploads/2016/03/020.jpg');
            height: 257px;
          }
          .card-6 {
            background-image: url('https://432351-1355208-raikfcquaxqncofqfm.stackpathdns.com/wp-content/uploads/2016/03/026.jpg');
            height: 257px;
          }

          .card-8 {
            background-image: url('https://432351-1355208-raikfcquaxqncofqfm.stackpathdns.com/wp-content/uploads/2016/03/036.jpg');
            height: 257px;
          }
          .card-9 {
            background-image: url('https://432351-1355208-raikfcquaxqncofqfm.stackpathdns.com/wp-content/uploads/2016/03/051.jpg');
            height: 257px;
          }
        }
      }
    }
  }
</style>
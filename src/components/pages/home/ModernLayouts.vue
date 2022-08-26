<template>
  <section class='modern-layouts'>
    <v-container>
      <div class="columns">
        <div class="column column-1">
          <div class="head">
            <span class="section-title">You Can Design Clean And Modern Grid Layouts</span>
            <p class="paragraph">
              Grids are the backbone of all layouts, infographics and presentations
            </p>
          </div>
          <v-card
            flat
            class="card-1"
          >
            <span>Studio</span>
            <router-link to="#">
              <span>More details</span>
              <v-icon>play_arrow</v-icon>
            </router-link>
          </v-card>
        </div>
        
        <div class="column column-2">
          <v-card
            flat
            class="card-2"
          >
            <span>Apartment</span>
            <router-link to="#">
              <span>More details</span>
              <v-icon>play_arrow</v-icon>
            </router-link>
          </v-card>

          <v-card
            flat
            class="card-3"
          >
            <span>Single Family Home</span>
            <router-link to="#">
              <span>More details</span>
              <v-icon>play_arrow</v-icon>
            </router-link>
          </v-card>

          <v-card
            flat
            class="card-4"
          >
            <span>Shop</span>
            <router-link to="#">
              <span>More details</span>
              <v-icon>play_arrow</v-icon>
            </router-link>
          </v-card>
        </div>

        <div class="column column-3">
          <v-card
            flat
            class="card-5"
          >
            <span>Office</span>
            <router-link to="#">
              <span>More details</span>
              <v-icon>play_arrow</v-icon>
            </router-link>
          </v-card>

          <v-card
            flat
            class="card-6"
          >
            <span>Villa</span>
            <router-link to="#">
              <span>More details</span>
              <v-icon>play_arrow</v-icon>
            </router-link>
          </v-card>
        </div>
      </div>
    </v-container>
  </section>
</template>

<script>
  export default {
    name: 'ModernLayouts',
  };
</script>

<style lang='scss' scoped>
  .modern-layouts {
    padding: 100px 0;

    .columns {
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 30px;
      @media (max-width: 992px) {
        flex-wrap: wrap;
      }

      .column {
        // global
        .v-card {
          display: flex;
          flex-direction: column;
          justify-content: space-between;
          position: relative;
          padding: 30px;
          border-radius: 4px;
          overflow: hidden;
          background-size: cover;
          background-repeat: no-repeat;
          background-position: center;
          width: 275px;
          @media (max-width: 620px) {
            width: 300px !important;
            height: 230px !important;
          }

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

          span {
            position: relative;
            font-size: 1.25rem;
            font-weight: 300;
            color: var(--white-color);
          }

          a {
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: relative;
            &:hover {
              padding: 0 10px;
            }

            span {
              font-size: .75rem;
              font-weight: 300;
              color: var(--white-color);
              text-transform: uppercase;
            }

            .v-icon {
              font-size: 1.4rem;
              color: var(--white-color);
            }
          }

          &.card-1 {
            background-image: url('@/assets/images/pages/home/modern-layouts/img-1.jpg');
            height: 580px;
          }

          &.card-2 {
            background-image: url('@/assets/images/pages/home/modern-layouts/img-2.jpg');
            height: 275px;
            margin-bottom: 25px;
          }
          &.card-3 {
            background-image: url('@/assets/images/pages/home/modern-layouts/img-3.jpg');
            height: 215px;
            margin-bottom: 25px;
          }
          &.card-4 {
            background-image: url('@/assets/images/pages/home/modern-layouts/img-4.jpg');
            height: 275px;
          }
          &.card-5 {
            background-image: url('@/assets/images/pages/home/modern-layouts/img-5.jpg');
            height: 588px;
            margin-bottom: 25px;
          }
          &.card-6 {
            background-image: url('@/assets/images/pages/home/modern-layouts/img-6.jpg');
            height: 200px;
          }
        }

        &.column-1 {
          .head {
            width: 275px;
            
            .section-title {
              display: block;
              font-size: 1.875rem;
              font-weight: 400;
              line-height: 1.3em;
              color: var(--dark-color);
              margin-bottom: 10px;
            }
            .paragraph {
              font-size: 1.125rem;
              font-weight: 300;
              color: var(--secondary-color);
              line-height: 1.5em;
              margin-bottom: 30px;
            }
          }
        }
      }
    }
  }
</style>
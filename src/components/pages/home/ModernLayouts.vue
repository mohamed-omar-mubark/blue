<template>
  <section class='modern-layouts'>
    <v-container>
      <v-row>
        <div class="column column-1 col-md-4 col-sm-6 col-12">
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
            left bottom
          </v-card>
        </div>
        
        <div class="column column-2 col-md-4 col-sm-6 col-12">
          <v-card
            flat
            class="card-2"
          >
            center top
          </v-card>

          <v-card
            flat
            class="card-3"
          >
            center center
          </v-card>

          <v-card
            flat
            class="card-4"
          >
            center bottom
          </v-card>
        </div>

        <div class="column column-3 col-md-4 col-sm-6 col-12">
          test
        </div>
      </v-row>
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

    .head {
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

    .v-card {
      padding: 30px;
      border-radius: 0;
      min-width: 275px;
      background-size: cover;
      background-repeat: no-repeat;
      background-position: center;

      &.card-1 {
        background-image: url('@/assets/images/pages/home/modern-layouts/img-1.jpg');
        min-height: 580px;
      }

      &.card-2 {
        background-image: url('@/assets/images/pages/home/modern-layouts/img-2.jpg');
        min-height: calc(100% /3);
      }
      &.card-3 {
        background-image: url('@/assets/images/pages/home/modern-layouts/img-3.jpg');
        min-height: calc(100% /3);
      }
      &.card-4 {
        background-image: url('@/assets/images/pages/home/modern-layouts/img-4.jpg');
        min-height: calc(100% /3);
      }
    }
  }
</style>
<template>
  <v-footer class='footer'>
    <v-container>
      <v-row>
        <div class="col-lg-3 col-md-6 col-sm-6">
          <div class="column">
            <span class="column-title d-block">About Site</span>
            <p>
              Blue is an real estate web app built by <strong>Mohamed Omar</strong> with Vue 2, Vuetify.
            </p>
            <router-link to="#" class="read-more">Read more</router-link>
          </div>
        </div>

        <div class="col-lg-3 col-md-6 col-sm-6">
          <div class="column">
            <span class="column-title d-block">Contact Us</span>
            <div class="contact-box">
              <v-icon>mail_outline</v-icon>
              <a href="mailto: mohamed.omar.mubark@gmail.com">mohamed.omar.mubark@gmail.com</a>
            </div>
            <div class="contact-box">
              <v-icon>call</v-icon>
              <a href="tel: +201201456635">+20 12 014 566 35</a>
            </div>
            <div class="contact-box">
              <a href="#">Contact us</a>
            </div>
          </div>
        </div>

        <div class="col-lg-6 col-md-12">
          <div class="column">
            <span class="column-title d-block">Newsletter</span>
            <div class="newsletter-input">
              <input type="email" placeholder="Enter your email">
              <button>Submit</button>
            </div>
            <p>
              Blue is a premium WordPress theme for real estate where modern aesthetics are combined with tasteful simplicity.
            </p>
          </div>
        </div>
      </v-row>
    </v-container>
  </v-footer>
</template>

<script>
  export default {
    name: 'Footer',
  };
</script>

<style lang='scss' scoped>
  .footer {
    padding: 100px 0 70px;
    background-color: var(--main-color);

    .column {
      .column-title {
        font-size: 1.125rem;
        font-weight: 500;
        color: var(--white-color);
        line-height: 1.5em;
        margin-bottom: 25px;
      }

      p {
        font-size: .875rem;
        font-weight: 300;
        color: var(--white-color);
        line-height: 1.5em;
        margin-bottom: 15px;
      }

      .read-more {
        font-size: 0.875rem;
        font-weight: 500;
        color: var(--white-color);
        &:hover {
          padding: 0 5px;
        }
      }

      .contact-box {
        display: flex;
        justify-content: start;
        align-items: center;
        gap: 10px;
        padding: 5px 0;

        .v-icon {
          font-size: 1.2rem;
          color: var(--white-color);
        }

        a {
          font-size: 0.875rem;
          color: var(--white-color);
          &:hover {
            padding: 0 5px;
          }
        }
      }

      .newsletter-input {
        display: flex;
        justify-content: start;
        align-items: flex-start;
        gap: 30px;
        @media (max-width: 575px) {
          flex-direction: column;
          gap: 0;
        }
        
        input {
          padding: 10px 12px;
          margin-bottom: 20px;
          border: none;
          border-radius: 4px;
          min-width: 360px;
          background-color: var(--white-color);
          font-size: 0.9375rem;
          font-weight: 400;
          color: var(--dark-color);
          transition: 0.3s;
          &:focus {
            outline: none;
          }
        }

        button {
          padding: 10px 30px;
          margin-bottom: 20px;
          border: none;
          border-radius: 4px;
          background-color: var(--info-color);
          font-size: 0.9375rem;
          font-weight: 400;
          color: var(--white-color);
        }
      }
    }
  }
</style>
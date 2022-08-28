<template>
  <section class='custom-form'>
    <v-container>
      <div class="overlay"></div>
      <v-row>
        <div class="col-xl-6 col-lg-6 col-md-6 col-sm-12 col-12">
          <div class="text-content">
            <span class="main-title">Create Custom Capture Forms And Manage Leads With The Integrated BLUE CRM</span>
            <p class="paragraph">
              The Inquiry Form widget allows you to design unique forms to capture your leads. It connects with BLUE CRM and your email inbox to keep your work everything on track.
            </p>
          </div>
        </div>

        <div class="col-xl-6 col-lg-6 col-md-6 col-sm-12 col-12">
          <h1>Form In progress</h1>
        </div>
      </v-row>
    </v-container>
  </section>
</template>

<script>
  export default {
    name: 'CustomForm',
  };
</script>

<style lang='scss' scoped>
  .custom-form {
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 100px 0;
    min-height: 930px;
    background-image: url('https://default.houzez.co/wp-content/uploads/2020/03/007.jpg');
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

    .text-content {
      position: relative;
      display: flex;
      flex-direction: column;
      justify-content: start;
      align-items: flex-start;
      gap: 10px;
      height: 100%;
      padding-bottom: 30px;

      &::after {
        position: absolute;
        content: '';
        bottom: 0;
        left: 0;
        width: 25%;
        height: 1px;
        background-color: var(--white-color);
        border-radius: 2000px;
      }

      .main-title {
        font-size: 2.1875rem;
        font-weight: 400;
        color: var(--white-color);
      }
      
      .paragraph {
        font-size: 1.125rem;
        font-weight: 300;
        line-height: 1.5em;
        color: var(--white-color);
      }
    }

    h1 {
      position: relative;
      color: var(--white-color);
    }
  }
</style>
<template>
  <section class='custom-form'>
    <v-container>
      <div class="overlay"></div>
      <div class="columns">
        <div class="column">
          <div class="text-content">
            <span class="main-title">Create Custom Capture Forms And Manage Leads With The Integrated BLUE CRM</span>
            <p class="paragraph">
              The Inquiry Form widget allows you to design unique forms to capture your leads. It connects with BLUE CRM and your email inbox to keep your work everything on track.
            </p>
          </div>
        </div>

        <div class="column">
          <div class="form-content">
            <v-form>
              <v-row>
                <v-col
                  class="d-flex"
                  cols="12"
                >
                  <v-select
                    :items="items"
                    label="Inquiry Type"
                    outlined
                  ></v-select>
                </v-col>

                <v-col
                  class="d-flex"
                  cols="12"
                >
                  <v-select
                    :items="informations"
                    label="Your Informations"
                    outlined
                  ></v-select>
                </v-col>

                <v-col
                  cols="12"
                  sm="6"
                >
                  <v-text-field
                    label="First Name"
                    outlined
                  ></v-text-field>
                </v-col>

                <v-col
                  cols="12"
                  sm="6"
                >
                  <v-text-field
                    label="Last Name"
                    outlined
                  ></v-text-field>
                </v-col>

                <v-col
                  cols="12"
                >
                  <v-text-field
                    label="Email Address"
                    outlined
                    type="email"
                  ></v-text-field>
                </v-col>

                <v-col
                  class="d-flex"
                  cols="12"
                >
                  <v-select
                    :items="property_details"
                    label="Property Details"
                    outlined
                  ></v-select>
                </v-col>

                <v-col
                  cols="12"
                  sm="6"
                >
                  <v-text-field
                    label="Max price"
                    outlined
                    type="number"
                  ></v-text-field>
                </v-col>

                <v-col
                  cols="12"
                  sm="6"
                >
                  <v-text-field
                    label="Minimum size (Sq Ft)"
                    outlined
                    type="number"
                  ></v-text-field>
                </v-col>

                <v-col
                  cols="12"
                  sm="6"
                >
                  <v-text-field
                    label="Number of beds"
                    outlined
                    type="number"
                  ></v-text-field>
                </v-col>

                <v-col
                  cols="12"
                  sm="6"
                >
                  <v-text-field
                    label="Number of baths"
                    outlined
                    type="number"
                  ></v-text-field>
                </v-col>

                <v-btn block>
                  Submit
                </v-btn>
              </v-row>
            </v-form>
          </div>
        </div>
      </div>
    </v-container>
  </section>
</template>

<script>
  export default {
    name: 'CustomForm',
    data() {
      return {
        items: ['Purchase', 'Rent', 'Sell', 'Miss', 'Evaluation'],
        informations: ["I'm a", "I'm a real estate agent", "I'm a property owner"],
        property_details: ['Apartment', 'Lot', 'Condo', 'Shop', 'Office', 'Villa']
      }
    }
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

    .columns {
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 100px;
      @media (max-width: 1200px) {
        flex-wrap: wrap;
      }

      .column {
        max-width: 550px;
        width: 100%;

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

        .form-content {
          position: relative;
          background-color: var(--white-color);
          border-radius: 2px;
          padding: 50px;
          @media (max-width: 575px) {
            padding: 40px 20px;
          }

          .col-12 {
            padding: 0 12px;
          }

          .v-btn {
            background-color: var(--info-color);
            border: none;
            box-shadow: none;
            padding: 15px 30px;
            font-size: 1rem;
            font-weight: 400;
            color: var(--white-color);
          }
        }
      }
    }
  }
</style>
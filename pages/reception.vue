<template>
  <v-main>
    <section id="locationtop">
      <v-row no-gutters>
        <v-img
          :src="require('@/assets/bar.jpeg')"
          min-height="'calc(100vh - ' + $vuetify.application.top + 'px)'"
          :height="$vuetify.breakpoint.smAndDown ? 700 : 800"
        >
          <v-container fill-height>
            <v-row align="center" class="white--text mx-auto" justify="center">
              <v-col class="white--text text-center" cols="12">
                <h2 class="display-2 font-weight-bold mb-3">Reception</h2>
                <v-responsive
                  class="mx-auto title font-weight-light mb-8"
                  max-width="720"
                  >Northside Farm, Horsley, NE15 0LZ</v-responsive
                >
              </v-col>
            </v-row>
          </v-container>
        </v-img>
      </v-row>
    </section>
    <section id="events" class="grey lighten-3">
      <div class="py-12"></div>

      <v-container class="text-center">

        <v-row>
          <v-col cols="12" md="12">
            <v-card class="py-12 px-6" color="grey lighten-5" flat>
              <v-theme-provider light>
                <div>
                  <v-avatar color="primary" size="88">
                    <font-awesome-icon icon="glass-cheers" />
                  </v-avatar>
                </div>
              </v-theme-provider>

              <v-card-title
                class="justify-center font-weight-black text-uppercase"
                >Reception</v-card-title
              >

              <v-card-subtitle class="subtitle-1">
                7pm until late
              </v-card-subtitle>

              <v-card-text class="text"
                >Join us for dinner, drinks and dancing
              </v-card-text>
            </v-card>
          </v-col>
        </v-row>
      </v-container>

      <div class="py-12"></div>
    </section>
    <section id="other" class="">
      <div class="py-12"></div>
      <v-container class="text-center">
        <h2 class="display-2 font-weight-bold mb-3">Details</h2>
        <v-responsive class="mx-auto mb-12" width="56">
          <v-divider class="mb-1"></v-divider>

          <v-divider></v-divider>
        </v-responsive>
        <v-simple-table>
          <template v-slot:default>
            <tbody>
              <tr>
                <td>Food</td>
                <td>
                  A reception meal will be served. Vegan or Allergy-friendly
                  meals available only with advance request via RSVP card
                </td>
              </tr>
              <tr>
                <td>Drinks</td>
                <td>Northside Farm has a bar on site</td>
              </tr>
              <tr>
                <td>Children</td>
                <td>
                  For our wedding day we would prefer family and bridal party
                  children only please
                </td>
              </tr>
              <tr>
                <td>Gifts</td>
                <td>
                  After 11 years we already have our home filled with everything
                  we need, so your presence on our day is the most important
                  thing but if you would like to give something, we'd really
                  appreciate a contribution towards our honeymoon
                </td>
              </tr>
              <tr>
                <td>Accomodation</td>
                <td>
                  Please see
                  <NuxtLink to="/accomodation">Accomodation</NuxtLink> for more
                  information
                </td>
              </tr>
              <tr>
                <td>Sunday</td>
                <td>
                  As we have the venue all weekend we're hosting a chilled out,
                  BYOB, self-catered day on the Sunday, you're more than welcome
                  to join us, children and dogs welcome too. The barn is open in
                  case of bad weather but we don't have any catering attending
                  and the bar may be closed so bring everything for your day
                </td>
              </tr>
            </tbody>
          </template>
        </v-simple-table>
        <div class="py-12"></div>
      </v-container>
      <div class="py-12"></div>
    </section>
  </v-main>
</template>

<script>
export default {
  name: 'Reception',
  data() {
    return {}
  },
}
</script>

<style lang="scss" scoped>
tbody {
     tr:hover {
        background-color: transparent !important;
     }
  }
</style>

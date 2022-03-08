<template>
  <v-main>
    <section id="locationtop">
      <v-row no-gutters>
        <v-img
          :src="require('@/assets/dining.jpeg')"
          min-height="'calc(100vh - ' + $vuetify.application.top + 'px)'"
          :height="$vuetify.breakpoint.smAndDown ? 700 : 800"
        >
          <v-container fill-height>
            <v-row align="center" class="mx-auto" justify="center">
              <v-col class="text-center" cols="12">
                <h2 class="display-2 font-weight-bold mb-3">Details</h2>
              </v-col>
            </v-row>
          </v-container>
        </v-img>
      </v-row>
    </section>

    <section id="events" class="grey lighten-3">
      <div class="py-12"></div>

      <v-container class="text-center">
        <h2 class="display-2 font-weight-bold mb-3">The Wedding Weekend</h2>

        <v-responsive class="mx-auto mb-12" width="56">
          <v-divider class="mb-1"></v-divider>

          <v-divider></v-divider>
        </v-responsive>

        <v-row>
          <v-col
            v-for="({ icon, title, text, details }, i) in events"
            :key="i"
            cols="12"
            md="6"
          >
            <v-card class="py-12 px-4" color="grey lighten-5" flat>
              <v-theme-provider light>
                <div>
                  <v-avatar color="primary" size="88">
                    <v-icon large v-text="icon"></v-icon>
                  </v-avatar>
                </div>
              </v-theme-provider>

              <v-card-title
                class="justify-center font-weight-black text-uppercase"
                v-text="title"
              ></v-card-title>

              <v-card-subtitle class="subtitle-1" v-text="text">
              </v-card-subtitle>

              <v-card-text class="text" v-text="details"> </v-card-text>
            </v-card>
          </v-col>
        </v-row>
      </v-container>

      <div class="py-12"></div>
    </section>

    <section id="timetable" class="">
      <div class="py-12"></div>
      <v-container class="text-center">
        <h2 class="display-2 font-weight-bold mb-3">Approx Timetable</h2>
        <v-responsive class="mx-auto mb-12" width="56">
          <v-divider class="mb-1"></v-divider>

          <v-divider></v-divider>
        </v-responsive>
        <v-simple-table>
          <template v-slot:default>
            <tbody>
              <tr>
                <td>11:00</td>
                <td>
                  Bar opens for guests, get ready, do your final checks and be
                  seated on either side in the gingang
                </td>
              </tr>
              <tr>
                <td>12:00</td>
                <td>Ceremony Time followed by drinks in the bar area</td>
              </tr>
              <tr>
                <td>15:00</td>
                <td>Its time for food in the main barn ​</td>
              </tr>
              <tr>
                <td>19:00</td>
                <td>
                  Please welcome our DJ, photobooth and evening guests. Its
                  party time! ​
                </td>
              </tr>
              <tr>
                <td>00:00</td>
                <td>
                  The bar has closed, its time to head home and get ready to
                  nurse that hangover ​
                </td>
              </tr>
            </tbody>
          </template>
        </v-simple-table>
        <div class="py-12"></div>
      </v-container>
    </section>

    <section id="other" class="grey lighten-3">
      <div class="py-12"></div>
      <v-container class="text-center">
        <h2 class="display-2 font-weight-bold mb-3">Other</h2>
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
                  A wedding breakfast and a reception meal will be served. Vegan
                  or Allergy-friendly meals available only with advance request
                  via RSVP card ​
                </td>
              </tr>
              <tr>
                <td>Drinks</td>
                <td>
                  Northside Farm has a bar on site, for the toast and table
                  drinks non-alcoholic options are available available only with
                  advance request via RSVP card ​
                </td>
              </tr>
              <tr>
                <td>Children</td>
                <td>
                  For our wedding day we would prefer family and bridal party
                  children only please, but if this would prevent you from
                  joining us, please get in touch. ​
                </td>
              </tr>
              <tr>
                <td>Gifts</td>
                <td>
                  After 11 years we already have our home filled with everything
                  we need, so your presence on our day is the most important
                  thing but if you would like to give something, we'd really
                  appreciate a contribution towards our honeymoon ​
                </td>
              </tr>
              <tr>
                <td>Pods</td>
                <td>
                  For more information there's a video tour of the inside on
                  their facebook page
                  <a href="https://fb.watch/bCZ2ZNpaqo/">here</a> and further
                  details
                  <a href="https://northsidefarm.co.uk/wigwams.html">here.</a>
                  Bookings are going through us, so
                  <NuxtLink to="/contact">Contact Us</NuxtLink> for more
                  information or to book ​
                </td>
              </tr>
              <tr>
                <td>Sunday</td>
                <td>
                  As we have the venue all weekend we're hosting a chilled out,
                  BYOB, self-catered day on the Sunday, you're more than welcome
                  to join us, children and dogs welcome too. The barn is open in
                  case of bad weather but we don't have any catering attending
                  and the bar may be closed so bring everything for your day ​
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
  name: 'Details',
  data() {
    return {
      events: [
        {
          icon: 'mdi-bag-suitcase',
          title: 'Friday',
          text: 'We welcome those staying in pods, tiny cottages or camping to the venue',
          details:
            "Check-in from 4pm unless you want to help set up, if camping bring all your equipment, if you're staying in the pods they have a bed base, mini fridge, kettle and toaster  and theres a shared kitchen but you need to bring the rest, including bedding/sleeping bags.",
        },
        {
          icon: 'mdi-crowd',
          title: 'Saturday',
          text: 'Its Our Wedding Day! Join us in celebrations, food, drinks and dancing',
          details:
            'Ceremony time is 12:00, bar will be open from 11am. Followed by the wedding breakfast, and an evening reception until late',
        },
        {
          icon: 'mdi-grill',
          title: 'Sunday',
          text: 'Northside Farm is ours for the whole weekend so we will be spending Sunday at the venue for an optional, self-catered, BYOB chill out day if you wish to join us.',
          details: 'Children and Dogs welcome on Sunday',
        },
        {
          icon: 'mdi-human-greeting',
          title: 'Monday',
          text: 'Happy campers its time to go home',
          details: 'We must vacate the site by TBC am',
        },
      ],
    }
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
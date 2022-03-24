<template>
  <v-main>
    <section id="locationtop">
      <v-row no-gutters>
        <v-img
          :src="require('@/assets/podoutside.jpg')"
          min-height="'calc(100vh - ' + $vuetify.application.top + 'px)'"
          :height="$vuetify.breakpoint.smAndDown ? 700 : 800"
        >
          <v-container fill-height>
            <v-row align="center" class="white--text mx-auto" justify="center">
              <v-col class="white--text text-center" cols="12">
                <h2 class="display-2 font-weight-bold mb-3">Accomodation</h2>
                <v-responsive
                  class="mx-auto title font-weight-light mb-8"
                  max-width="720"
                  >Horsley, NE15 0LZ</v-responsive
                >
              </v-col>
            </v-row>
          </v-container>
        </v-img>
      </v-row>
    </section>

    <section id="onsiteoptions">
      <div class="py-12"></div>

      <v-container>
        <h2 class="display-2 font-weight-bold mb-3 text-center">
          On-Site Accomodation
        </h2>

        <v-responsive class="mx-auto mb-12" width="56">
          <v-divider class="mb-1"></v-divider>

          <v-divider></v-divider>
        </v-responsive>

        <v-row>
          <v-col cols="12" md="4">
            <v-img
              :src="require('@/assets/podoutside.jpg')"
              class="mb-4"
              height="275"
              max-width="100%"
            ></v-img>

            <h3 class="font-weight-black mb-4 text-uppercase">Glamping Pod</h3>

            <p class="title font-weight-light mb-5">
              Insulated camping wigwams with beds and a mini kitchen
            </p>

            <p class="title font-weight-light mb-5">Sleeps: 5</p>

            <p class="title font-weight-light mb-5">£200</p>

            <v-btn class="ml-n4 font-weight-black" href="/accomodation#pods"
              >More Info</v-btn
            >
          </v-col>
          <v-col cols="12" md="4">
            <v-img
              :src="require('@/assets/cottages.jpg')"
              class="mb-4"
              height="275"
              max-width="100%"
            ></v-img>

            <h3 class="font-weight-black mb-4 text-uppercase">
              Fairytale Cottages
            </h3>

            <p class="title font-weight-light mb-5">
              Fully equiped, ensuite Cottages are currently all sold out
            </p>

            <p class="title font-weight-light mb-5">Sleeps: 2</p>

            <p class="title font-weight-light mb-5">£275+</p>

            <v-btn class="ml-n4 font-weight-black" href="/accomodation#cottages"
              >More Info</v-btn
            >
          </v-col>
          <v-col cols="12" md="4">
            <v-img
              :src="require('@/assets/tent.jpg')"
              class="mb-4"
              height="275"
              max-width="100%"
            ></v-img>

            <h3 class="font-weight-black mb-4 text-uppercase">Camping</h3>

            <p class="title font-weight-light mb-5">
              Bring your tent and camping gear and stay 1, 2 or 3 nights
            </p>

            <p class="title font-weight-light mb-5">Sleeps: ?</p>

            <p class="title font-weight-light mb-5">£15pp/pn</p>

            <v-btn class="ml-n4 font-weight-black" href="/accomodation#camping"
              >More Info</v-btn
            >
          </v-col>
        </v-row>
      </v-container>

      <div class="py-12"></div>
    </section>

    <section id="offsiteoptions" class="grey lighten-3">
      <div class="py-12"></div>
      <v-container class="text-center">
       <h2 class="display-2 font-weight-bold mb-3 text-center">
          Other Accomodation
        </h2>
        <v-responsive class="mx-auto mb-12" width="56">
          <v-divider class="mb-1"></v-divider>

          <v-divider></v-divider>
        </v-responsive>

        <p>
          We have no deals or preference with any offsite accomodation
          suppliers, so here's a selection of nearby places that may be suitable
        </p>

        <v-simple-table>
          <template v-slot:default>
            <thead>
              <tr>
                <th class="text-center">Location</th>
                <th class="text-center">Approx Travel Time</th>
              </tr>
            </thead>
            <tbody>
              <tr v-for="item in offsideoptions" :key="item.location">
                <td>{{ item.location }}</td>
                <td>{{ item.traveltime }}</td>
              </tr>
            </tbody>
          </template>
        </v-simple-table>
        <div class="py-12"></div>
      </v-container>
      <div class="py-12"></div>
    </section>

    <section id="pods">
      <div class="py-12"></div>
      <v-container class="text-center">
        <h2 class="display-2 font-weight-bold mb-3 text-center">Glamping Pods</h2>
        <v-responsive class="mx-auto mb-12" width="56">
          <v-divider class="mb-1"></v-divider>

          <v-divider></v-divider>
        </v-responsive>

            <v-img
              :src="require('@/assets/podoutside.jpg')"
              class="mb-4"
              height="275"
              max-width="100%"
            ></v-img>

            <p>Pod hire is £200 for 3 nights Fri-Mon</p>
            <p>Sleeps maximum of 5</p>
            <p>
              1 XL bed (converted from sofas and table) and 1 single, fridge,
              toaster, kettle, microwave, heater, fire pit, picnic table,
              outside tap
            </p>
            <p>Bring your own sleeping and cooking equipment</p>
            <p>
              A full kitchen, dining space and 4 family bathrooms are a short
              walk away
            </p>
            <p>Contact us for booking, not available on their website</p>
            
                <v-btn color="grey" href="/contact" outlined large>
                  <span class="grey--text text--darken-1 font-weight-bold"
                    >Contact Us</span
                  >
                </v-btn>
             
                <v-btn
                  color="grey"
                  href="https://www.northsidefarm.co.uk/thewigwams.html"
                  outlined
                  large
                >
                  <span class="grey--text text--darken-1 font-weight-bold"
                    >Northside Website</span
                  >
                </v-btn>
            

      </v-container>
    </section>
    <section id="cottages">
      <div class="py-12"></div>
      <v-container class="text-center">
        <h2 class="display-2 font-weight-bold mb-3">Fairytale Cottages</h2>
        <v-responsive class="mx-auto mb-12" width="56">
          <v-divider class="mb-1"></v-divider>

          <v-divider></v-divider>
        </v-responsive>
       
            <v-img
              :src="require('@/assets/cottages.jpg')"
              class="mb-4"
              height="275"
              max-width="100%"
            ></v-img>
            <p>
              Fairytale Cottage hire is £275 for 2 nights and £350 for 3 nights
            </p>
            <p>Sleeps 2</p>
            <p>
              Double bed, ensuite bathroom, kitchen with hob, microwave, mini
              fridge, patio area
            </p>
            <p>Bedding and some kitchenware supplied</p>
            <p>Cottages are currently sold out</p>
           
                <v-btn color="grey" href="/contact" outlined large>
                  <span class="grey--text text--darken-1 font-weight-bold"
                    >Contact Us</span
                  >
                </v-btn>
            
                <v-btn
                  color="grey"
                  href="https://www.northsidefarm.co.uk/cottages.html"
                  outlined
                  large
                >
                  <span class="grey--text text--darken-1 font-weight-bold"
                    >Northside Website</span
                  >
                </v-btn>
              

      </v-container>
    </section>
    <section id="camping">
      <div class="py-12"></div>
      <v-container class="text-center">
        <h2 class="display-2 font-weight-bold mb-3">Camping</h2>
        <v-responsive class="mx-auto mb-12" width="56">
          <v-divider class="mb-1"></v-divider>

          <v-divider></v-divider>
        </v-responsive>

            <v-img
              :src="require('@/assets/tent.jpg')"
              class="mb-4"
              height="275"
              max-width="100%"
            ></v-img>
            <p>Limited onsite Camping available</p>
            <p>Bring your tent and all your camping gear</p>
            <p>
              If your tent is more than a 2 man, we'd prefer you to set up on
              the Friday, even if you don't stay until the Saturday
            </p>
            <p>
              A full kitchen, dining space and 4 family bathrooms are a short
              walk away
            </p>
            <p>
              Please get in touch for camping or if you'd like to borrow some
              equipment
            </p>
           
                <v-btn color="grey" href="/contact" outlined large>
                  <span class="grey--text text--darken-1 font-weight-bold"
                    >Contact Us</span
                  >
                </v-btn>

      </v-container>
    </section>
  </v-main>
</template>

<script>
export default {
  name: 'Accomodation',
  data() {
    return {
      offsideoptions: [
        {
          location: 'Wylam - e.g. The Ship Inn',
          traveltime: '10min',
        },
        {
          location: 'Matfen Hall',
          traveltime: '11min',
        },
        {
          location: 'Close House',
          traveltime: '12min',
        },
        {
          location: 'Corbridge - e.g. Duke of Wellington',
          traveltime: '15min',
        },
        {
          location: 'Granary Inn',
          traveltime: '16min',
        },
        {
          location: 'NCL Airport',
          traveltime: '20min',
        },
        {
          location: 'Hexham',
          traveltime: '21min',
        },
        {
          location: 'Newcastle City Centre',
          traveltime: '25min',
        },
        {
          location: 'Whitley Bay',
          traveltime: '40min',
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
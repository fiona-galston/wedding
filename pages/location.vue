<template>
  <v-main>
    <section id="locationtop">
      <v-row no-gutters>
        <v-img
          :src="require('@/assets/tractor.jpg')"
          min-height="'calc(100vh - ' + $vuetify.application.top + 'px)'"
          :height="$vuetify.breakpoint.smAndDown ? 700 : 800"
        >
          <v-container fill-height>
<v-row
                  align="center"
                  class="white--text mx-auto"
                  justify="center"
                >
                  <v-col
                    class="white--text text-center"
                    cols="12"
                  >
            <h2 class="display-2 font-weight-bold mb-3">Northside Farm</h2>
                  </v-col>
</v-row>
          </v-container>
        </v-img>
      </v-row>
    </section>

    <section id="wherehowfar" class="grey lighten-3">
      <div class="py-12"></div>

      <v-container class="text-center">
        <h2 class="display-2 font-weight-bold mb-3">Location</h2>

        <v-responsive class="mx-auto mb-12" width="56">
          <v-divider class="mb-1"></v-divider>

          <v-divider></v-divider>
        </v-responsive>

        <v-row>
          <v-col cols="6">
            <v-img
          :src="require('@/assets/map.jpeg')"/>
          </v-col>
          <v-col cols="6">
            <div>
              <h2>Northside Farm</h2>
              <p>Horsley, Northumberland, NE15 0LZ</p>
            </div>
            <div>
              <a href="https://www.google.com/maps/place/Northside+Farm/@55.0032617,-1.8660044,13.97z/data=!4m5!3m4!1s0x487ddbcf505ab397:0x4e3c8d772456f63!8m2!3d55.0013199!4d-1.8620034">Go to Google Maps</a>
            </div>
            <div class="py-12"></div>

            </v-col>
        </v-row>
        <v-row>
          <v-col cols="12">
<div>
  <h2>How Far is it?</h2>
          <v-simple-table>
    <template v-slot:default>
      <thead>
        <tr>
          <th class="text-center">
            Location
          </th>
          <th class="text-center">
            Approx Travel Time
          </th>
        </tr>
      </thead>
      <tbody>
        <tr
          v-for="item in distances"
          :key="item.location"
        >
          <td>{{ item.location }}</td>
          <td>{{ item.traveltime }}</td>
        </tr>
      </tbody>
    </template>
  </v-simple-table>
</div>
          </v-col>
        </v-row>
      </v-container>

      <div class="py-12"></div>
    </section>

  </v-main>
</template>

<script>
export default {
  name: 'Location',
  data () {
      return {
        distances:[
          {
            location: 'NCL Airport',
            traveltime: '20min'
          },{
            location: 'Hexham',
            traveltime: '21min'
          },{
            location: 'Newcastle City Centre',
            traveltime: '25min'
          },{
            location: 'Whitley Bay',
            traveltime: '40min'
          },
        ],
      }
    },



methods: {

}
}
</script>
<style lang="scss" scoped>
tbody {
     tr:hover {
        background-color: transparent !important;
     }
  }
</style>
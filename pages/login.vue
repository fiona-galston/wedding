<template>
  <v-main>
    <section id="hero">
      <v-row no-gutters>
        <v-img
          :src="require('@/assets/housekeepingview.jpg')"
          min-height="'calc(100vh - ' + $vuetify.application.top + 'px)'"
          :height="$vuetify.breakpoint.smAndDown ? 700 : 800"
        >
          <v-container fill-height>
            <v-row align="center" class="white--text mx-auto" justify="center">
              <v-col class="white--text text-center" cols="6">
                <span
                  :class="[
                    $vuetify.breakpoint.smAndDown ? 'display-1' : 'display-2',
                  ]"
                  class="font-weight-light"
                >
                  <v-card class="py-12 px-4" color="grey lighten-5" flat>
                    <v-form>
                      <v-container>
                        <v-row>
                          <v-col cols="12" md="12">
                            <p>Daytime Details</p>

                            <v-text-field
                              v-model="password"
                              type="password"
                              label="Enter Password"
                              required
                            ></v-text-field>
                            <p class="text--secondary caption">
                              Please note this uses cookies, only enter password
                              and submit if you consent to use of cookies
                            </p>
                            <v-btn
                              color="success"
                              class="mr-4"
                              @click="loginUser"
                            >
                              Submit
                            </v-btn>
                            <v-btn
                              color="danger"
                              class="mr-4"
                              @click="removeAuthorisation"
                            >
                              Cancel
                            </v-btn>
                          </v-col>
                        </v-row>
                      </v-container>
                    </v-form>
                  </v-card>
                </span>
              </v-col>
            </v-row>
          </v-container>
        </v-img>
      </v-row>
    </section>
  </v-main>
</template>

<script>
export default {
  name: 'Login',
  data() {
    return {
      password: '',
      isAuthorised: false,
    }
  },
  methods: {
    loginUser(){
      if(this.$passwordProtect.authorise(this.password)){
      this.isAuthorised = this.$passwordProtect.isAuthorised()
      this.$router.push(this.redirectPath)
      }
      else{
        alert('Incorrect password, please check your ceremony invitation for password')
        this.password = ''
      }
    },
    removeAuthorisation() {
      this.$passwordProtect.removeAuthorisation()
      this.isAuthorised = this.$passwordProtect.isAuthorised()
      this.$router.push('/')
    },
  },
  computed: {
    redirectPath() {
      const path = this.$route.query.previousPath
      return path || '/'
    },
  },
}
</script>


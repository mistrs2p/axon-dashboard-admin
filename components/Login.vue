<template>
  <div class="pa-2 pa-md-4 flex-grow-1 align-center justify-center d-flex flex-column">
    <div class="layout-content ma-auto w-full">
      <div>
        <v-card class="text-center pa-1 justify-center display-1 mb-2">
          <v-card-title class="justify-center display-1 mb-2">Welcome</v-card-title>
          <v-card-subtitle>Sign in to your account</v-card-subtitle>
          <v-card-text>
            <v-form>
              <v-text-field
                label="Email"
                outlined
              ></v-text-field>

              <v-text-field
                label="Password"
                outlined
                :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off' "
                :type="showPassword ? 'text' : 'password' "
                @click:append="showPassword = !showPassword"
              ></v-text-field>

              <v-btn class="mb-2 primary" dark block x-large>Sign In</v-btn>

              <div class="caption font-weight-bold text-uppercase my-3">Or sign in with</div>

              <v-btn href="/" class="my-5 primary lighten-2" dark block x-large>
                <v-icon left>mdi-google</v-icon>
                Google
              </v-btn>
              <v-btn href="/" class="my-5 primary lighten-2" dark block x-large>
                <v-icon left>mdi-facebook</v-icon>
                Facebook
              </v-btn>
              <div class="mt-5"><a href="/"> Forgot password? </a></div>
            </v-form>
          </v-card-text>
        </v-card>
        <div class="text-center mt-6"> Don't have an account? <a href="/" class="font-weight-bold"> Create one here </a></div>
      </div>
      <div class="overline mt-4">Lux Admin PRO - 1.5.1</div>
    </div>
  </div>
</template>

<script>
export default {
  data ()  {
    return {
      showPassword: false
    }
  }
}
</script>

<style scoped>
  .layout-content {
    max-width: 480px;
  }
</style>
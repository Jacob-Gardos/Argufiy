<template>
  <b-card body-border-variant="border" class="shadow-sm" body-bg-variant="light">
    <b-row>
      <!-- Side Title -->
      <b-col
        order="2"
        order-md="1"
        class="d-flex flex-column align-items-center justify-content-center p-md-5"
        md="6"
      >
        <h2 class="d-none d-md-flex">
          <logoFull />
          <span class="pl-2 text-muted">Login</span>
        </h2>
      </b-col>
      <!-- Register Email / Password -->
      <b-col order="1" order-md="2" cols="12" md="6">
        <b-form-group id="fieldset-2">
          <label for="emailInput">
            <strong>Email</strong>
          </label>
          <b-form-input id="emailInput" type="email" trim></b-form-input>
        </b-form-group>
        <b-form-group id="fieldset-3">
          <label for="passwordInput">
            <strong>Password</strong>
          </label>
          <b-form-input id="passwordInput" type="password" trim></b-form-input>
          <small class="text-muted">
            Dont Have An Account ?
            <router-link to="register">Register</router-link>
          </small>
        </b-form-group>
        <b-button block variant="primary">Login</b-button>
        <div class="my-auto w-100 d-flex flex-column">
          <small class="text-muted text-center p-2">Or Login With A Provider</small>
          <b-button block>
            <googleIcon class="float-left" :size="20" />
            <span>Sign In With Google</span>
          </b-button>
        </div>
      </b-col>
    </b-row>
  </b-card>
</template>

<script>
import logoFull from '~/components/core/logoFull'
import googleIcon from 'vue-material-design-icons/Google.vue'

export default {
  name: 'loginCard',
  components: {
    logoFull,
    googleIcon
  }
}
</script>

<style lang="scss" scoped>
</style>
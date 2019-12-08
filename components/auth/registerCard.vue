<template>
  <b-card body-border-variant="border" body-bg-variant="light">
    <b-row>
      <!-- Register Google -->
      <b-col
        order="2"
        order-md="1"
        class="d-flex flex-column align-items-center justify-content-center p-md-5"
        md="6"
      >
        <h2 class="d-none d-md-flex mb-auto">
          <logoFull />
          <span class="pl-2 text-muted">Register</span>
        </h2>
        <div class="my-auto w-100 d-flex flex-column">
          <small class="text-muted text-center p-2">Or Register With A Provider</small>
          <b-button block>
            <googleIcon class="float-left" :size="20" />
            <span>Sign Up With Google</span>
          </b-button>
        </div>
      </b-col>
      <!-- Register Email / Password -->
      <b-col order="1" order-md="2" cols="12" md="6">
        <b-form-group id="fieldset-1">
          <label for="nameInput">
            <strong>Display Name</strong>
          </label>
          <b-form-input id="nameInput" trim></b-form-input>
        </b-form-group>
        <b-form-group id="fieldset-2">
          <label for="emailInput">
            <strong>Email</strong>
          </label>
          <b-form-input id="emailInput" trim></b-form-input>
        </b-form-group>
        <b-form-group
          id="fieldset-3"
          description="Passwords must contain at least eight characters, including at least 1 letter and 1 number."
        >
          <label for="passwordInput">
            <strong>Password</strong>
          </label>
          <b-form-input id="passwordInput" trim></b-form-input>
        </b-form-group>
        <b-button block variant="primary">Sign Up</b-button>
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
<template>
  <b-row class="h-100" align-h="center" align-v="center">
    <b-col cols="12" md="10">
      <loginCard />
    </b-col>
  </b-row>
</template>

<script>
import loginCard from '~/components/auth/loginCard.vue'

export default {
  name: 'login',
  layout: 'auth',
  components: {
    loginCard
  }
}
</script>

<style lang="scss" scoped>
</style>
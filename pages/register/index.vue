<template>
  <b-row class="h-100" align-h="center" align-v="center">
    <b-col cols="12" md="10">
      <registerCard />
    </b-col>
  </b-row>
</template>

<script>
import registerCard from '~/components/auth/registerCard'

export default {
  name: 'registerPage',
  layout: 'auth',
  components: {
    registerCard
  }
}
</script>

<style lang="scss" scoped></style>

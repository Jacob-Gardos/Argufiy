<template>
  <div class="h-100">
    <appBar />
    <b-container class="h-100">
      <nuxt />
    </b-container>
  </div>
</template>

<script>
import appBar from '~/components/core/appBar'

export default {
  name: 'auth',
  components: {
    appBar
  }
}
</script>

<style lang="scss" >
@import '../assets/main.scss';
</style>
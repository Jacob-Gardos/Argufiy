<template>
  <div>
    <appBar />
    <b-container class="mt-sm-0 mt-md-2 h-100" :fluid="this.$breakpoints.sMd">
      <nuxt />
    </b-container>
  </div>
</template>

<script>
import appBar from '~/components/core/appBar'

export default {
  components: {
    appBar
  }
}
</script>

<style lang="scss" >
@import '../assets/main.scss';
</style>

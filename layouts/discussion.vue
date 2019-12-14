<template>
  <div>
    <appBar />
    <b-container class="mt-sm-0 mt-md-2">
      <nuxt />
    </b-container>
  </div>
</template>

<script>
import appBar from '~/components/core/appBar'

export default {
  name: 'discussion',
  components: {
    appBar
  }
}
</script>

<style lang="scss" >
@import '../assets/main.scss';
</style>
<template>
  <!-- Topic Title Bar -->
  <b-row>
    <b-col md="2" class="px-0 px-xl-3"></b-col>
    <b-col cols="12" md="8" class="px-0">
      <discussionCard />
      <h2>{{$route.params.id}}</h2>

      <hr />
    </b-col>
  </b-row>
</template>

<script>
import logo from '~/components/core/logo'
import discussionCard from '~/components/discussion/discussionCard'

export default {
  name: 'index',
  layout: 'discussion',
  components: {
    discussionCard
  }
}
</script>

<style  scoped>
</style>
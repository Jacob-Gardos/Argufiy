<template>
  <b-list-group class="flex-row flex-md-column categoryCol">
    <b-list-group-item href="#" v-for="(topic, index) in topics" :key="index">
      {{
      topic.name
      }}
    </b-list-group-item>
  </b-list-group>
</template>

<script>
export default {
  name: 'categoryCol',
  data() {
    return {
      topics: [
        { name: 'Politics' },
        { name: 'Science' },
        { name: 'Tech' },
        { name: 'Gaming' },
        { name: 'Politics' },
        { name: 'Science' },
        { name: 'Tech' },
        { name: 'Gaming' }
      ]
    }
  }
}
</script>

<style  scoped>
.categoryCol::-webkit-scrollbar {
  display: none;
}

.flex-row {
  overflow-x: scroll !important;
  white-space: nowrap !important;
}
</style>

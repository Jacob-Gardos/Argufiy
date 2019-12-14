<template>
  <b-card
    footer-bg-variant="white"
    footer-border-variant="0"
    footer-class="pt-0"
    style="cursor: pointer;"
    @click="openDiscussion"
  >
    <!-- Card Title -->
    <b-card-title class="d-flex">
      <span class="font-weight-bold text-capitalize" :class="'text-' + prop1Color">{{ prop1 }}</span>
      <span class="text-danger font-weight-bolder font-italic">!</span>
      <span class="font-weight-bold text-capitalize" :class="'text-' + prop2Color">{{ prop2 }}</span>
    </b-card-title>

    <!-- Data And Preview -->
    <b-row>
      <!-- Data Desktop -->
      <b-col cols="auto" class="d-md-flex align-items-center">
        <div class="text-center rounded outlined box text-white" :class="'bg-' + leadProp.color">
          <span class="font-weight-bold align-self-center align-middle">{{ leadProp.percent }}%</span>
          <span
            class="align-middle text-capitalize d-inline-block text-truncate"
            style="max-width: 55px;"
          >{{ leadProp.name }}</span>
        </div>
      </b-col>

      <!-- Preview Paragraph -->
      <b-col class="px-0 px-md-3">
        <b-card-text>{{ previewText }}</b-card-text>
      </b-col>
    </b-row>

    <!-- Footer -->
    <template v-slot:footer>
      <small class="text-muted">
        <CommentIcon :size="20" />1.6k
      </small>
      <small class="text-muted">
        <PersonIcon :size="20" />38
      </small>
      <small class="text-muted float-right">Last post 3 mins ago</small>
    </template>
  </b-card>
</template>

<script>
import PersonIcon from 'vue-material-design-icons/Account.vue'
import CommentIcon from 'vue-material-design-icons/Comment.vue'

export default {
  name: 'topicCard',
  props: {
    prop1: String,
    prop1Color: String,
    prop1Percent: Number,
    prop2: String,
    prop2Color: String,
    prop2Percent: Number,
    previewText: String
  },
  computed: {
    leadProp() {
      if (this.prop1Percent > this.prop2Percent) {
        return {
          color: this.prop1Color,
          percent: this.prop1Percent,
          name: this.prop1
        }
      } else {
        return {
          color: this.prop2Color,
          percent: this.prop2Percent,
          name: this.prop2
        }
      }
    }
  },

  methods: {
    openDiscussion() {
      this.$router.push({ name: 'discussion-id', params: { id: 5098546 } })
    }
  },

  components: {
    CommentIcon,
    PersonIcon
  }
}
</script>

<style scoped>
.topicCard-text {
  display: -webkit-box;
  -webkit-line-clamp: 3;
  -webkit-box-orient: vertical;
  overflow: hidden;
  text-overflow: ellipsis;
}

.box {
  width: 60px;
  height: 60px;
}

.card-text {
  display: -webkit-box;
  -webkit-line-clamp: 3;
  -webkit-box-orient: vertical;
  overflow: hidden;
  text-overflow: ellipsis;
}
</style>

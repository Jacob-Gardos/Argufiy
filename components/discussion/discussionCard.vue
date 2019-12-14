<template>
  <b-card
    overlay
    img-src="https://s.marketwatch.com/public/resources/images/MW-HL036_aborti_ZH_20190607132847.jpg"
    img-alt="Card Image"
    style="height: 200px;"
    class="topicTrendCard d-flex flex-column border-0"
    text-variant="white"
  >
    <b-card-title>
      <span>Abortion</span>
      <logo />
      <span>ProLife</span>
    </b-card-title>
    <b-card-sub-title sub-title-text-variant="light">Who has had the best political campaign ?</b-card-sub-title>
  </b-card>
</template>

<script>
import logo from '~/components/core/logo'

export default {
  name: 'discussionCard',
  components: {
    logo
  }
}
</script>

<style scoped>
.topicTrendCard {
  height: 200px !important;
  overflow: hidden;
}

.topicTrendCard .card-img {
  position: absolute !important;
  left: 50% !important;
  top: 50% !important;
  transform: translate(-50%, -50%) !important;
}
.card-body .card-img-overlay {
  background-color: black;
}

.card-body {
  display: flex;
  flex-direction: column;
}

.card-title {
  margin-top: auto;
}

.card-img-overlay {
  height: 100%;
  background: rgb(0, 0, 0);
  background: linear-gradient(
    0deg,
    rgba(0, 0, 0, 0.8883928571428571) 0%,
    rgba(0, 0, 0, 0.7539390756302521) 26%,
    rgba(0, 0, 0, 0.29175420168067223) 79%
  );
}
</style>
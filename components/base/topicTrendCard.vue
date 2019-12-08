<template>
  <div class="my-3">
    <span class="text-sm-left d-none d-sm-flex text-muted p-2">Trending This Week</span>
    <b-card-group columns class="my-2 mt-md-0">
      <b-card
        overlay
        img-src="https://ksassets.timeincuk.net/wp/uploads/sites/54/2017/01/ps4-vs-switch-vs-xbox-1.jpg"
        img-alt="Card Image"
        style="height: 200px;"
        class="topicTrendCard d-flex flex-column"
        text-variant="white"
        title="Xbox Vs PS4"
        sub-title="Which Console Is Worth Your Money ?"
      ></b-card>
      <b-card
        overlay
        img-src="https://a57.foxnews.com/media2.foxnews.com/BrightCove/694940094001/2019/10/09/931/524/694940094001_6093520306001_6093516479001-vs.jpg?ve=1&tl=1"
        img-alt="Card Image"
        style="height: 200px;"
        title="Trump Vs Hiliary"
        class="topicTrendCard d-none d-sm-block"
        sub-title="Who has a better political campaign"
        text-variant="white"
      ></b-card>
      <b-card
        overlay
        img-src="https://hackr.io/blog/react-vs-vue/thumbnail/large"
        img-alt="Card Image"
        style="height: 200px;"
        title="Vue Vs React"
        class="topicTrendCard d-none d-sm-block"
        sub-title="Which Is Best For Web Dev In 2019"
        text-variant="white"
      ></b-card>
    </b-card-group>
  </div>
</template>

<script>
export default {
  name: 'topicTrendCard'
}
</script>

<style scoped>
.topicTrendCard .card-img {
  height: inherit !important;
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
<template>
  <div class="card">
    <div class="image-container">
      <img class="image-card" :src="imageCard">
    </div>
    <div class="text-card">
      <div class="title">{{nameCard}}Title</div>
      <p class="rating">
        <span>{{ratingCard}}</span>
      </p>
      <p class="description">{{descriptionCard}}Description</p>

      <div class="button-container">
        <button class="watch" id="watch" @click="goToShowPage">WATCH</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SearchCard",
  props: {
    idCard: "",
    nameCard: String,
    imageCard: String,
    ratingCard: Number,
    descriptionCard: String
  },
  data: function() {
    return {};
  },
  methods: {
    goToShowPage() {
      this.$router.push({ path: "/show-page/" + this.idCard });
    }
  }
};
</script>

<style scoped>
</style>
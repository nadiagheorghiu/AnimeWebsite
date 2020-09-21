<template>
  <section class="search-collection">
    <div class="cards-list">
      <SearchCard/>
      <SearchCard/>
    </div>
  </section>
</template>

<script>
import SearchCard from "./SearchCard.vue";
export default {
  name: "SearchCollection",
  components: {
    SearchCard
  }
};
</script>

<style scoped>
</style>
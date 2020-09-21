<template>
  <div>
    <SearchPageForm/>
    <SearchCollection/>
  </div>
</template>

<script>
import SearchPageForm from "./components/SearchPageForm.vue";
import SearchCollection from "./components/SearchCollection";
export default {
  name: "SearchPage",
  components: {
    SearchPageForm,
    SearchCollection
  }
};
</script>

<style scoped>
</style>

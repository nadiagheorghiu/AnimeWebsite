<template>
  <div class="box">
    <section class="collection-container">
      <BrowseHeaderCollection CollectionName="smth"/>
      <div class="cards-container">
        <BrowseCard/>
        <BrowseCard/>
        <BrowseCard/>
        <BrowseCard/>
        <BrowseCard/>
      </div>
    </section>
  </div>
</template>

<script>
import BrowseCard from "./BrowseCard.vue";
import BrowseHeaderCollection from "./BrowseHeaderCollection.vue";
export default {
  name: "BrowseCollection",
  components: {
    BrowseCard,
    BrowseHeaderCollection,
    props: { Collection: String }
  }
};
</script>

<style scoped>
.box {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
}
.collection-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin-top: 12px;
  margin-bottom: 12px;
}
.cards-container {
  flex-wrap: wrap;
  display: flex;
  justify-content: center;
  width: 100%;
}
</style>
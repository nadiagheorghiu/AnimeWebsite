<template>
  <div>
    <HeroSection :description="heroShow.description"/>
    <BrowseCollection topicCollection="Most Popular"/>
    <BrowseCollection topicCollection="Newest"/>
    <BrowseCollection topicCollection="Recently Updated"/>
    <MoreAnime/>
  </div>
</template>

 
<script>
import MoreAnime from "./components/MoreAnime.vue";
import HeroSection from "./components/HeroSection.vue";
import BrowseCollection from "./components/BrowseCollection.vue";
export default {
  name: "HomePage",
  components: {
    HeroSection,
    BrowseCollection,
    MoreAnime
  },
  data: function() {
    return {
      heroShow: {
        description:
          "The most recent My Hero Academia film, Heroes Rising takes class 1-A to a new setting called Nabu Island for hero training in the wake of All Might’s retiremen. Of course, things fail to go to plan, and a group of villains -- including one with the power to steal quirks -- storms the island. Without any pro heroes to save them, it’s up to Class 1-A to protect the island’s citizens, even in the face of a terrifying power that feels eerily similar to All For One"
      }
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
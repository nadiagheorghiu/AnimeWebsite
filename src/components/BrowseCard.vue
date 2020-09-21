<template>
  <div>
    <router-link to="#">
      <div class="browse-card">
        <img class="portrait" :src="`${browseCardImg}`" alt="Anime Poster">
        <span>{{browseCardTitle}}</span>
      </div>
    </router-link>
  </div>
</template>

<script>
export default {
  name: "BrowseCard",
  data: function() {
    return {
      browseCardImg:
        "https://s.ecrater.com/stores/426122/5a68e6084f2e9_426122n.jpg",
      browseCardTitle: "Hero Academia"
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.portrait {
  margin-top: 5px;
  width: 90%;
  height: 75%;
}
.browse-card {
  width: 9em;
  height: 15em;
  font-size: 1em;
  color: rgb(0, 0, 0);
  margin: 10px;
  overflow: hidden;
  overflow-wrap: break-word;
  text-overflow: ellipsis;
  font-weight: 700;
}

a {
  text-decoration: none;
}
</style>
<template>
  <div class="collection-header">
    <h2>{{CollectionName}}</h2>
    <span class="see-more">
      <router-link tag="span" to="#">See More ></router-link>
    </span>
  </div>
</template>

<script>
export default {
  name: "BrowseHeaderCollection",

  props: {
    CollectionName: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.collection-header {
  display: flex;
  justify-content: space-between;
  flex-direction: row;
  width: 100%;
  margin-bottom: 10px;
  font-size: 1.5em;
  height: 1.7em;
  margin-bottom: 20px;
}
.collection-header h2,
.see-more {
  margin: 10px;
}
.collection-header h2 {
  text-align: left;
}

.see-more {
  cursor: pointer;
  text-align: right;
}
.see-more:hover {
  text-decoration: underline;
}
</style>
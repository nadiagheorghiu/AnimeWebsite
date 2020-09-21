<template>
  <div class="moreAnime">
    <div class="moreAnimeText"></div>
    <h2>Looking for more anime?</h2>
    <h3>Browse all Anime</h3>
    <div class="container">
      <button class="btn_moreAnime">Browse All</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "MoreAnime"
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

<style scoped>
.moreAnime {
  padding: 100px 50px;
  position: relative;
  width: 100%;
  min-height: 40vh;
  padding: 0 100px;
  
  background-position: center;
  background-size: cover;
}

h2 {
  text-align: center;
  font-size: 35px;
  padding-top: 10px;
  color: var(--first-color);
}
h3 {
  text-align: center;
  padding-top: 8px;
  font-size: 30px;
}
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  padding-top: 15px;
}
.btn_moreAnime {
  padding: 10px;
  font-size: 18px;
  border-radius: 20px;
  border: 3px solid var(--first-color);
  cursor: pointer;
  display: inline-block;
  letter-spacing: 2.5px;
}

.btn_moreAnime:hover {
  background: var(--first-color);
  color: #fff;
  transition: 0.5s;
}
</style>
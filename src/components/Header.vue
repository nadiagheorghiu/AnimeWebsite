<template>
  <div>
    <header>
      <div class="header">
        <router-link to="/" class="logo">
          <img src="../assets/logo1.png" alt="Search">
        </router-link>
        <nav class="navigation">
          <ul>
            <li>
              <router-link class="links" to="/category-page/most-popular">Most Popular</router-link>
            </li>
            <li>
              <router-link class="links" to="/category-page/newest">Newest</router-link>
            </li>
            <li>
              <router-link class="links" to="/category-page/recently-updated">Recently Updated</router-link>
            </li>
            <li>
              <router-link class="search-icon" to="/search">
                <img src="assets/search_icon.png" alt="Search">
              </router-link>
            </li>
          </ul>
        </nav>
      </div>
    </header>
  </div>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {};
  }
};
</script>


<style scoped>
* {
  font-family: var(--font-family);
}
header {
  height: 80px;
  display: flex;
  justify-content: center;
  flex-direction: row;
}
.header {
  width: 1100px;
  display: flex;
  align-content: space-between;
  flex-direction: row;
}

.search-icon img {
  width: 25px;
}
.links {
  text-decoration: none;
  padding: 20px;
  font-size: 20px;
  color: #3a392b;
}

nav {
  width: 77vw;
  margin-left: 10px;
  align-content: flex-end;
  justify-content: flex-end;
  display: flex;
}
nav ul {
  list-style: none;
  margin-top: 25px;
  display: flex;
}

nav ul :hover {
  color: #e67e22;
}

.logo {
  width: 50px;
  height: auto;
  display: flex;
  padding: 5px;
}

.logo img {
  margin: 5px 0 0 27px;
  width: 100px;
}

@media (max-width: 450px) {
}
</style>

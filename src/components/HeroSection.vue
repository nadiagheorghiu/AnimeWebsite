<template>
  <div class="banner">
    <div class="content">
      <h1>Comming Soon!</h1>
      <h2>
        My hero Academia:
        <span>Heroes Rising</span>
      </h2>

      <div>
        <p class="description" :class="{seeAll: see}">{{description}}</p>
        <button class="ReadMore" v-if="!see" @click="ReadMore">
          <span>Read more</span>
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HeroSection",
  props: {
    description: String
  },
  data: function() {
    return {
      see: false
    };
  },
  methods: {
    ReadMore: function() {
      this.see = true;
    }
  }
};
</script>


<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: var(--font-family);
}

.ReadMore{
   padding: 10px;
   border-radius: 20px;
   border: 3px solid var(--first-color);
   cursor: pointer;
 }
 .ReadMore:hover{
   background: var(--first-color);
   color: #fff;
   transition: 0.5s;
 }
.banner {
  padding: 100px 50px;
  position: relative;
  width: 100%;
  min-height: 85vh;
  padding: 0 100px;
  background-image: url("/assets/2.jpg");
  background-position: center;
  background-size: cover;
}
.banner .content {
  max-width: 700px;
}
.banner .content h1 {
  padding: 50px 25px;
  text-transform: uppercase;
  font-weight: 600;
  font-size: 3em;
  letter-spacing: 0.25em;
  color: var(--first-color);
  margin-bottom: 20px;
}
.banner .content h2 {
  text-transform: uppercase;
  font-weight: 300;
  font-size: 2.5em;
  letter-spacing: 0.1em;
  color: rgb(221, 210, 210);
  margin-bottom: -10px;
}
.banner .content h2 span {
  font-weight: 800;
}
.banner .content p {
  font-size: 1.2em;
  font-weight: 300;
  letter-spacing: 0.02em;
  line-height: 1.5em;
  color: #fff;
  margin: 15px 0 35px;
}
.seeAll{
--n-of-lines: ;
}
p{
  --n-of-lines: 4;
  --line-height: 1.2em;
  line-height: var(--line-height);
  max-height: calc(var(--line-height) * var(--n-of-lines));
  overflow: hidden;
  text-overflow: ellipsis;
  display: block;
  }
.seeAll {
  --n-of-lines: ;
}

@media (max-width: 991px) {
  .banner {
    padding: 100px 50px;
  }
  .banner .content {
  max-width: 350px;
}
.banner .content h1 {
  padding: 15px 5px;
  font-size: 2.5em;
  letter-spacing: 0.2em;
  margin-bottom: 15px;
}
  .banner .content h2 {
    font-weight: 350;
    font-size: 2em;
    letter-spacing: 0.05em;
  }
  .banner .content p {
    font-size: 1em;
  }
}


@media (max-width: 750px) {
   
  .banner .content {
  max-width: 320px;
}
 
}

@media (max-width: 450px) {
  .banner {
    padding: 100px 50px;
  }
 .banner .content h1 {
  padding: 15px 5px;
  font-size: 2em;
  letter-spacing: 0.2em;
  margin-bottom: 15px;
}
  .banner .content {
  max-width: 250px;
}
  .banner .content h2 {
    font-weight: 300;
    font-size: 1.5em;
    letter-spacing: 0.05em;
  }
  .banner .content p {
    font-size: 1em;
  }
}
</style>

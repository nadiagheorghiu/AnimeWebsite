<template>
  <footer class="footer">
    <div class="footer-container">
      <div class="footer-logo">
        <img src="../assets/logo.png" alt="logo" width="65px" height="65px">
      </div>
      <ul class="footer-nav">
        <li>
          <router-link class="links" to="#">Home</router-link>
        </li>
        <li>
          <router-link class="links" to="#">Home</router-link>
        </li>
        <li>
          <router-link class="links" to="#">Home</router-link>
        </li>
      </ul>
      <ul class="footer-secondary-nav">
        <li>
          <router-link class="links" to="#">Most popular</router-link>
        </li>
        <li>
          <router-link class="links" to="#">Newest</router-link>
        </li>
        <li>
          <router-link class="links" to="#">Recently Updated</router-link>
        </li>
      </ul>
      <div class="contact-block">
        <h3>We're happy to hear from you!</h3>
        <a href="tel:0040723472221">
          <i class="fas fa-phone"></i> 0040723472221
        </a>
        <a href="mailto:ngheorghiu31@gmail.com">ngheorghiu31@gmail.com</a>
      </div>
      <div class="newsletter">
        <div class="newsletter-text">
          <div class="icon"></div>
          <p>Subscribe to our Newsletter</p>
        </div>
        <div class="text-input">
          <form action="post">
            <input type="email" name="Enter Your Email Address" size="20">
            <input type="submit" value="Submit">
          </form>
        </div>
      </div>
      <div class="social-networks">
        <h3>Share our content!</h3>
        <div class="facebook">
          <a href="#" target="_bank">
            <img src="../assets/facebook.png" alt="Facebook Logo" width="30px" height="30px">
          </a>
        </div>
        <div class="twitter">
          <a href="#" target="_bank">
            <img src="../assets/twitter.png" alt="Twitter Logo" width="30px" height="30px">
          </a>
        </div>
        <div class="instagram">
          <a href="#" target="_bank">
            <img src="/assets/instagram.png" alt="Instagram Logo" width="30px" height="30px">
          </a>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
  data() {
    return {};
  }
};
</script>

<style>
* {
  padding: 0;
  margin: 0;
}
li {
  list-style-type: none;
}
a {
  text-decoration: none;
}
body {
  font-family: var(--font-family);
}
h1,
h2,
h3,
h4,
h5,
h6 {
  font-family: var(--font-family);
}
.footer {
  color: var(--first-color);
  background: rgb(14, 2, 48);
  padding: 4em 0;
  display: grid;
  grid-template-columns: 7vw 1fr 7vw;
  grid-template-rows: auto auto;
}

.footer-container {
  grid-column: 2 / 3;
}
.footer-container {
  grid-column: 2 / 3;
  display: grid;
  grid-template-columns: 2fr 2fr 2fr 3fr;
  grid-template-rows: auto auto;
  grid-template-areas: "logo navigation secondary social" "contact contact . newsletter";
}
.footer-logo {
  grid-area: logo;
}
.footer-nav {
  grid-area: navigation;
  justify-self: center;
}
.footer-secondary-nav {
  grid-area: secondary;
  justify-self: center;
}
.social-networks {
  grid-area: social;
}
.contact-block {
  grid-area: contact;
}
.newsletter {
  grid-area: newsletter;
}
.social-networks {
  grid-area: social;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: auto auto;
  justify-items: center;
}
.social-networks h3 {
  grid-column: 1 / -1;
}
.facebook {
  justify-self: right;
}
.instagram {
  justify-self: left;
}
.contact-block,
.newsletter {
  align-self: end;
}
.bottom-line {
  display: grid;
  grid-template-columns: 7vw 8fr 4fr 7vw;
}
.bottom-line p {
  grid-column: 2;
}
.footer a {
  color: #fff;
}
.contact-block a {
  display: block;
  border: 2px solid #fff;
  padding: 0.5rem;
  margin: 10px 0 0;
  text-align: center;
  width: 70%;
}
.contact-block a:hover {
  border: 2px solid var(--first-color);
  color: var(--first-color);
}
.social-networks {
  border-bottom: 2px solid var(--first-color);
}
.bottom-line {
  background-color: var(--second-color);
}
.bottom-line,
.bottom-line a {
  color: #fff;
}

@media screen and (min-width: 960px) {
  .footer {
    height: 45vh;
  }
}
@media screen and (max-width: 960px) {
  .footer-nav,
  .footer-secondary-nav {
    display: none;
  }
  .footer-container {
    grid-template-columns: 1fr 1fr;
    grid-template-rows: 20vh 25vh;
    grid-template-areas: "logo social" "contact newsletter";
  }
  .bottom-line {
    display: grid;
    grid-template-columns: 7vw 1fr 7vw;
  }
  .bottom-line p {
    justify-self: center;
  }
  .legal {
    grid-column: 2 / -2;
    justify-items: center;
  }
}
.newsletter-text,
.text-input {
  text-align: center;
}
.text-input input {
  border-radius: 0;
}
.text-input input:first-child {
  height: 2rem;
}
.text-input input:last-child {
  height: 2.25rem;
  color: #fff;
  border: none;
  background-color: var(--first-color);
  width: 5rem;
  font-weight: bold;
}
.fas,
.fab {
  font-size: 1.5rem;
}
.newsletter-text icon,
.newsletter-text p {
  margin: 0 0 1.1rem;
}
.newsletter-text p {
  line-height: 2rem;
}
@media screen and (max-width: 768px) {
  .footer-container {
    grid-template-columns: 1fr;
    grid-template-areas: "logo" "social" "newsletter" "contact";
  }
  .footer-logo,
  .contact-block {
    justify-self: center;
    align-self: center;
  }
  .social-networks,
  .newsletter {
    padding: 3rem 0;
  }
  .contact-block a,
  .contact-block p {
    margin: 0 auto;
  }
  .contact-block h3,
  .social-networks h3 {
    line-height: 3rem;
  }
}
</style>
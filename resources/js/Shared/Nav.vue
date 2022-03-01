<template>
  <nav class="navMenu">
    <NavLink class="NavLink" href="/" :active="$page.component === 'Home'"
      >Home</NavLink
    >
    <NavLink class="NavLink" href="/users" :active="$page.component === 'Users'"
      >About</NavLink
    >
    <NavLink
      class="NavLink"
      href="/settings"
      :active="$page.component === 'Settings'"
      >Pricing</NavLink
    >
    <NavLink
      class="NavLink"
      href="/settings"
      :active="$page.component === 'Settings'"
      >Contact</NavLink
    >
    <div class="dot"></div>
  </nav>
</template>

<script>
import NavLink from "./NavLink.vue";

export default {
  components: { NavLink },
};
</script>

<style scoped>
/* Codepen : https://codepen.io/WhisnuYs/pen/XWdpdGP */
@import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700&display=swap");
* {
  -webkit-box-sizing: border-box;
  box-sizing: border-box;
}

body {
  background: #272727;
  font-family: "Montserrat", sans-serif;
}

.navMenu {
  position: absolute;
  top: 5%;
  left: 50%;
  -webkit-transform: translate(-50%, -50%);
  transform: translate(-50%, -50%);
}

.navMenu .NavLink {
  color: #f6f4e6;
  text-decoration: none;
  font-size: 1.2em;
  text-transform: uppercase;
  font-weight: 600;
  display: inline;
  width: 100px;
  padding-inline: 10px;
  -webkit-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
}

.navMenu .NavLink:hover {
  color: #fddb3a;
}

.navMenu .dot {
  width: 6px;
  height: 6px;
  background: #fddb3a;
  border-radius: 50%;
  opacity: 0;
  -webkit-transform: translateX(30px);
  transform: translateX(30px);
  -webkit-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
}

.navMenu .NavLink:nth-child(1):hover ~ .dot {
  -webkit-transform: translateX(35px);
  transform: translateX(35px);
  -webkit-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  opacity: 1;
}

.navMenu .NavLink:nth-child(2):hover ~ .dot {
  -webkit-transform: translateX(110px);
  transform: translateX(110px);
  -webkit-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  opacity: 1;
}

.navMenu .NavLink:nth-child(3):hover ~ .dot {
  -webkit-transform: translateX(192px);
  transform: translateX(192px);
  -webkit-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  opacity: 1;
}

.navMenu .NavLink:nth-child(4):hover ~ .dot {
  -webkit-transform: translateX(288px);
  transform: translateX(288px);
  -webkit-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  opacity: 1;
}

@media screen and (max-width: 500px) {
  .navMenu .NavLink {
    float: none;
    display: block;
    text-align: left;
  }

  .header-right {
    float: none;
  }
}
</style>

<template>
  <div id="app">
    <div class="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/gallery">Gallery</router-link>
    </div>
    <router-view />
  </div>
</template>

<style>
:root {
  background: #c5cacd;
  font-family: 'Josefin Sans', sans-serif;
  color: #252525;
  position: relative;
}

.nav {
  position: absolute;
  top: 30px;
  left: 30px;
}

.nav a {
  color: #2c3e50;
  font-size: 24;
  font-weight: 400;
}

.nav a.router-link-exact-active {
  color: #42568b;
}
@media only screen and (max-width: 620px) {
  .nav {
    top: 95px;
    left: 30px;
  }
}
@media only screen and (max-width: 375px) {
  .nav {
    top: 65px;
  }
}
</style>

<template>
  <div id="app">
    <div class="nav">
      <a href="/">Home</a> |
      <a href="/gallery">Gallery</a>
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
  z-index: 100;
}

.nav a {
  color: #2c3e50;
  font-size: 24;
  font-weight: 400;
}

.nav a:active {
  color: #42568b;
}
@media only screen and (max-width: 620px) {
  .nav {
    margin: 20px;
    text-align: center;
  }
}
@media only screen and (max-width: 375px) {
  .nav {
    margin: 20px;
    text-align: center;
  }
}
</style>

<template>
  <div id="app">
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
  margin: 20px 0 -20px 0;
  text-align: center;
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
</style>

<template>
  <div class="main">
    <div class="grid-container">
      <div class="home">
        <div class="page">
          <div class="picture"><img src="../assets/images/me.jpg" class="headerImg" /></div>
          <div class="title">
            <div class="text">
              <p><b>Salih </b>Gümüş</p>
              <span>Developer </span>/
              <span> Amateur Photographer</span>
            </div>
          </div>
          <div class="hello"><h1 class="hello">Hello.</h1></div>
          <div class="description">
            <p class="parag">
              I'm a Computer Engineering student. I'm beginner full-stack developer and junior game
              developer. Also I'm an amateur photographer.
            </p>
            <div class="address">Adana/Turkey</div>
          </div>
          <div class="footer">
            <div class="left-icons">
              <a href="https://www.instagram.com/sudanmerinosu/" target="_blank">
                <i class="im im-instagram"></i>
              </a>
              <a href="https://www.linkedin.com/in/salihgumus/" target="_blank">
                <i class="im im-linkedin" />
              </a>
            </div>
            <div class="right-icons">
              <a href="https://twitter.com/sudanmerinosu" target="_blank">
                <i class="im im-twitter" />
              </a>
              <a href="https://github.com/sudanmerinosu" target="_blank">
                <i class="im im-github"></i>
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Home',
};
</script>

<style>
.main {
  display: flex;
  justify-content: center;
}

.grid-container {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-template-rows: repeat(3, 1fr);
  gap: 0px 0px;
  grid-template-areas:
    'home home home home'
    'home home home home'
    'home home home home';
}

.home {
  display: grid;
  grid-template-columns: repeat(7, 1fr);
  grid-template-rows: repeat(9, 1fr);
  gap: 0px 0px;
  grid-template-areas:
    '. . . . . '
    ' page page page page '
    ' page page page page '
    ' page page page page '
    ' page page page page '
    ' page page page page '
    ' page page page page '
    ' page page page page '
    '. . . . . ';
  grid-area: home;
}

.page {
  display: grid;
  grid-template-columns: repeat(6, 1fr);
  grid-template-rows: repeat(8, 1fr);
  gap: 0px 0px;
  grid-area: page;

  margin-top: 40px;

  background-color: white;
  -webkit-box-shadow: 0px 0px 50px -15px rgba(0, 0, 0, 0.75);
  -moz-box-shadow: 0px 0px 50px -15px rgba(0, 0, 0, 0.75);
  box-shadow: 0px 0px 50px -15px rgba(0, 0, 0, 0.75);
}

.picture {
  grid-area: 2 / 3 / 5 / 6;
  z-index: 1;
}
.headerImg {
  width: 309px;
  height: 309px;
}

.title {
  max-width: 100%;
  grid-area: 3 / 2 / 6 / 5;
  background-color: #e8e8e8;
  position: relative;
}
.text {
  position: absolute;
  top: 200px;
  left: 30px;
  letter-spacing: 2px;
  line-height: 15px;
  font-family: 'Oswald', sans-serif;
}
.text p {
  font-size: 24px;
}

.hello {
  max-width: 100%;
  grid-area: 6 / 1 / 7 / 3;
  font-family: Kalam;
  font-size: 42px;
  padding-left: 10px;
  padding-top: 2px;
}
.description {
  grid-area: 7 / 1 / 8 / 7;
  position: relative;
}
.parag {
  font-family: Kalam;
  font-size: 18px;
  font-weight: 400;
  position: absolute;
  bottom: 15px;
  padding: 30px;
}
.address {
  position: absolute;
  bottom: 0px;
  left: 225px;
  font-size: 24px;
}
.footer {
  grid-area: 8 / 1 / 9 / 7;
  position: relative;
}
.footer a {
  padding: 20px;
  color: black;
}
.left-icons {
  position: absolute;
  bottom: 10px;
  left: 225px;
}
.right-icons {
  position: absolute;
  bottom: 50px;
  left: 225px;
}
</style>

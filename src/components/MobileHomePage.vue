<template>
  <div class="main-mobile">
    <div class="grid-container-mobile">
      <div class="home-mobile">
        <div class="page-mobile">
          <div class="picture-mobile">
            <div class="header-picture"><img src="../assets/images/header.jpg" alt="" /></div>
          </div>
          <div class="title-mobile">
            <div class="text-mobile">
              <p><b>Salih </b>Gümüş</p>
              <span>Developer </span>/
              <span> Amateur Photographer</span>
            </div>
          </div>
          <div class="hello-description-mobile">
            <h1 class="hello-mobile">Hello.</h1>
            <div class="description-mobile">
              <p class="parag-mobile">
                I'm a Computer Engineering student. I'm mid-level Full-Stack developer and junior
                game developer. Also I'm an amateur photographer.
              </p>
              <div class="address-mobile">Adana/Turkey</div>
            </div>
          </div>
          <div class="footer-mobile">
            <div class="left-icons-mobile">
              <a href="https://www.instagram.com/sudanmerinosu/" target="_blank">
                <i class="im im-instagram"></i>
              </a>
              <a href="https://www.linkedin.com/in/salihgumus/" target="_blank">
                <i class="im im-linkedin" />
              </a>
            </div>
            <div class="right-icons-mobile">
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
export default {};
</script>

<style>
.main-mobile {
  background-color: white;
}
.grid-container-mobile {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-template-rows: repeat(3, 1fr);
  gap: 0px 0px;
  grid-template-areas:
    'home-mobile home-mobile'
    'home-mobile home-mobile'
    'home-mobile home-mobile';
}

.home-mobile {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: repeat(2, 1fr);
  gap: 0px 0px;
  grid-template-areas:
    'page-mobile page-mobile page-mobile'
    'page-mobile page-mobile page-mobile';
  grid-area: home-mobile;
}

.page-mobile {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: 0.5fr 1.5fr 0.2fr 1.2fr 1fr;
  gap: 0px 0px;
  grid-area: page-mobile;
}

.picture-mobile {
  grid-area: 2 / 2 / 3 / 3;
  z-index: 1;
}

.title-mobile {
  grid-area: 2 / 2 / 4 / 3;
  background-color: #e8e8e8;
  position: relative;
  top: 0px;
}
.text-mobile {
  position: absolute;
  bottom: 50px;
  left: 20px;
  letter-spacing: 2px;
  line-height: 15px;
  font-family: 'Oswald', sans-serif;
}

.hello-description-mobile {
  grid-area: 4 / 2 / 5 / 3;
  font-family: Kalam;
  font-size: 18px;
  padding-left: 10px;
  padding-top: 2px;
}
.address-mobile {
  font-size: 24px;
  display: flex;
  justify-content: center;
}

.footer-mobile {
  grid-area: 5 / 2 / 6 / 3;
}
.footer-mobile a {
  padding: 50px;
  color: black;
}
.left-icons-mobile {
  display: flex;
  justify-content: center;
}
.right-icons-mobile {
  display: flex;
  justify-content: center;
}
</style>

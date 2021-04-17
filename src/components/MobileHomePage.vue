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
  grid-template-columns: 1fr 1fr;
  grid-template-rows: 1fr 1fr 1fr;
  gap: 0px 0px;
  grid-template-areas:
    'home-mobile home-mobile'
    'home-mobile home-mobile'
    'home-mobile home-mobile';
}

.home-mobile {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-rows: 1fr 1fr;
  gap: 0px 0px;
  grid-template-areas:
    'page-mobile page-mobile page-mobile'
    'page-mobile page-mobile page-mobile';
  grid-area: home-mobile;
}

.page-mobile {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-rows: 1fr 0.4fr 1fr 1fr;
  gap: 0px 0px;
  grid-template-areas:
    '. picture-mobile .'
    '. title-mobile .'
    'hello-description-mobile hello-description-mobile hello-description-mobile'
    'footer-mobile footer-mobile footer-mobile';
  grid-area: page-mobile;
}

.picture-mobile {
  grid-area: picture-mobile;
  z-index: 1;
}

.title-mobile {
  grid-area: title-mobile;
  background-color: #e8e8e8;
  position: relative;
}
.text-mobile {
  position: absolute;
  top: 35px;
  left: 20px;
  letter-spacing: 2px;
  line-height: 15px;
  font-family: 'Oswald', sans-serif;
}

.hello-description-mobile {
  grid-area: hello-description-mobile;
  position: relative;
  font-family: Kalam;
  font-size: 18px;
  padding-left: 10px;
  padding-top: 2px;
}
.address-mobile {
  position: absolute;
  bottom: 100px;
  left: 110px;
  font-size: 24px;
}

.footer-mobile {
  grid-area: footer-mobile;
  position: relative;
}
.footer-mobile a {
  padding: 50px;
  color: black;
}
.left-icons-mobile {
  position: absolute;
  top: 0px;
  left: 60px;
  margin-left: auto;
  margin-right: auto;
}
.right-icons-mobile {
  position: absolute;
  top: 50px;
  left: 60px;

  margin-left: auto;
  margin-right: auto;
}
</style>

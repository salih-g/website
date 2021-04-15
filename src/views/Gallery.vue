<template>
  <div class="Gallery">
    <h1 class="title">Inside my world</h1>

    <div class="photo-grid">
      <div
        class="card card-tall"
        style="background-image:url('https://drive.google.com/uc?id=1q3LFPywJV-cB9B_HjrpAJhSz506dBZC3')"
      ></div>
      <div
        class="card card-tall"
        style="background-image:url('https://drive.google.com/uc?id=1n4EIi73kmXluHiXgat40v9SdCMeHkdE6')"
      ></div>
      <div
        class="card card-wide"
        style="background-image:url('https://drive.google.com/uc?id=1U1lxuPkUw_hChEqhnVku-ADCr0m89AaL')"
      ></div>

      <div
        class="card card-tall"
        style="background-image:url('https://drive.google.com/uc?id=1cozgceIALzGNNI-QMmHcP7d6wWnAFxpy')"
      ></div>
      <div
        class="card card-tall"
        style="background-image:url('https://drive.google.com/uc?id=1gUiVYFQS4WEKIpAIQVe8knikpMbLsQkM')"
      ></div>
      <div
        class="card card-wide card-tall"
        style="background-image:url('https://drive.google.com/uc?id=16s436l2TW4mfFwtYqPbzIIVIBzZsn2Lm')"
      ></div>
      <div
        class="card "
        style="background-image:url('https://drive.google.com/uc?id=1NL92vWNb5dEy5F1jatzIfQGpLlWLiJxJ')"
      ></div>

      <div
        class="card  card-wide"
        style="background-image:url('https://drive.google.com/uc?id=1JzL2f9wCFUkE05za29L_Z-qWv1yfzqqs')"
      ></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Gallery',
};
</script>

<style>
.title {
  display: flex;
  justify-content: center;
  font-size: 48px;
}
.card {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background: #353535;
  font-size: 3rem;
  color: #fff;
  box-shadow: rgba(3, 8, 20, 0.1) 0px 0.15rem 0.5rem, rgba(2, 8, 20, 0.1) 0px 0.075rem 0.175rem;
  height: 100%;
  width: 100%;
  border-radius: 4px;
  transition: all 500ms;
  overflow: hidden;

  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}

.card:hover {
  box-shadow: rgba(2, 8, 20, 0.1) 0px 0.35em 1.175em, rgba(2, 8, 20, 0.08) 0px 0.175em 0.5em;
  transform: translateY(-3px) scale(1.1);
}
.photo-grid {
  display: grid;
  gap: 1rem;

  grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
  grid-auto-rows: 240px;
}
@media screen and (min-width: 600px) {
  .card-tall {
    grid-row: span 2 / auto;
  }
  .card-wide {
    grid-column: span 2 / auto;
  }
}
</style>

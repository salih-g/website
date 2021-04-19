<template>
  <div class="gallery">
    <h1 class="titleGallery">
      Take a flight into my world
    </h1>

    <div class="photos">
      <div class="image" v-for="(image, index) in images" :key="index">
        <a :href="image" target="_blank">
          <img :src="image" />
        </a>
      </div>
    </div>
  </div>
</template>
<script>
// Viewport orientation if portrait 0 else 1
// width < heigh ⇒ portrait
// width > height ⇒ landscape

export default {
  name: 'Gallery',
  data() {
    return {
      accesKey: process.env.VUE_APP_SERVICE_ACCESS_KEY,
      url: 'https://api.unsplash.com/users/sudanmerinosu/photos?per_page=100&query=10&',
      images: {},
    };
  },
  methods: {
    fetchPictures() {
      fetch(`${this.url}client_id=${this.accesKey}`)
        .then((res) => res.json())
        .then((json) => {
          json.forEach((data, index) => {
            this.images[index] = data.urls.regular;
            this.$forceUpdate();
          });
        })
        .catch((err) => {
          console.error('error', err);
        });
    },
  },

  created() {
    this.fetchPictures();
    // console.log(this.images);
  },
};
</script>

<style>
.gallery {
  margin: 100px;
}
.titleGallery {
  text-align: center;
  padding-top: 20px;
}
.photos {
  position: relative;
  column-count: 3;
  padding: 20px;
}
.image {
  display: inline-block;
  overflow: hidden;
  box-shadow: rgba(3, 8, 20, 0.1) 0px 0.15rem 0.5rem, rgba(2, 8, 20, 0.1) 0px 0.075rem 0.175rem;
  border-radius: 4px;
  transition: all 500ms;
  overflow: hidden;
}
.image:hover {
  box-shadow: rgba(2, 8, 20, 0.1) 0px 0.35em 1.175em, rgba(2, 8, 20, 0.08) 0px 0.175em 0.5em;
  transform: translateY(-3px) scale(1.1);
}
img {
  width: 100%;
  transition: 0.5s ease-in-out;
}
.image:hover img {
  transform: scale(1.5);
}
@media screen and (max-width: 1024px) {
  .gallery {
    margin: 75px;
  }
  .photos {
    column-count: 2;
  }
}
@media screen and (max-width: 768px) {
  .gallery {
    margin: 50px;
  }
  .photos {
    column-count: 2;
  }
}
@media screen and (max-width: 375px) {
  .gallery {
    margin: 10px;
  }
  .photos {
    column-count: 1;
  }
}
</style>

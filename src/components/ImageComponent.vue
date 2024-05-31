<template>
  <div class="image_container image-wide image-tall">
    <img :src="resolve_url(isrc)" alt="ialt" loading="lazy" />
  </div>
</template>

<script>
export default {
  name: "ImageComponent",
  props: {
    isrc: String,
    ialt: String,
  },
  methods: {
    resolve_url: function (url) {
      return "https://" + url;
    },
  },
};
</script>

<style>
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

body {
  font-size: 18px;
}

.gallary_container {
  display: grid;
  gap: 1rem;
  grid-template-columns: repeat(auto-fit, minmax(15em, 1fr));
  grid-auto-rows: 15.5em;
  padding: 10px;
  margin-bottom: 3em;
  
}

.image_container img {
  /* width: 100%;
  height: 100%;
  box-shadow: #565656 0px 20px 30px -10px;
  object-fit: cover;
  transition: opacity 0.5s ease;
  opacity: 0.5;
  Faded effect */
  width: 90%;
  height: 90%;
  margin: 10px;
  border: 2.4px solid #ffffff;
  border-radius: 50px;
  -webkit-filter: blur();
  filter: blur(100%);
  transition-duration: 0.5s;
  opacity: 1;
}

.image_container img:hover {
  border: 5px solid #fff;
  -webkit-transform: scale(1.1);
  -ms-transform: scale(1.1);
  transform: scale(1.05);
  -webkit-filter: none;
  filter: none;
  border-radius: 0px;
  opacity: 0.5;
}


@media screen and (min-width: 768px) {
  .image-tall {
    grid-row: span 2 / auto;
  }

  .image-wide {
    grid-column: span 2 / auto;
  }
}

/* .gallary_container {
  display: flex;
  flex-wrap: wrap;
  margin: auto;
}
.image_container {
  flex: 0 0 auto;
  margin: 5px;
  overflow: hidden;
}

@media (min-width: 768px) {
  .image_container {
    display: block;
    width: auto;
    height: auto;
  }
} */
</style>

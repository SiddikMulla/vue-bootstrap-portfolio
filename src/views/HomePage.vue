<template>
    <h1 class="glow">𝓗𝓸𝓶𝓮 𝓟𝓪𝓰𝓮</h1>
  <div class="container carPos">
    <SliderImages />
  </div>

  <div class="mx-5 gallary_container">

    <ImageComponent v-for="(item, index) in items" :key="index" :isrc="item.src" :ialt="item.alt" />
  </div>
</template>

<script>
import ImageComponent from "@/components/ImageComponent.vue";
import SliderImages from "@/components/Carsoul.vue"
export default {
  name: "HomePage",
  components: { ImageComponent, SliderImages },
  data() {
    return {
      items: [
        { src: "picsum.photos/id/599/800/530", alt: "value2" },
        { src: "picsum.photos/400/300?random=1", alt: "value4" },
        {
          src: "picsum.photos/600/300?random=2",
          alt: "mosaic collection image",
        },
        {
          src: "picsum.photos/200/500?random=3",
          alt: "mosaic collection image",
        },
        {
          src: "picsum.photos/800/300?random=4",
          alt: "mosaic collection image",
        },
        {
          src: "picsum.photos/200/300?random=5",
          alt: "mosaic collection image",
        },
        {
          src: "picsum.photos/200/300?random=6",
          alt: "mosaic collection image",
        },
        {
          src: "picsum.photos/200/300?random=7",
          alt: "mosaic collection image",
        },
        {
          src: "picsum.photos/200/300?random=8",
          alt: "mosaic collection image",
        },
        {
          src: "picsum.photos/200/300?random=9",
          alt: "mosaic collection image",
        },
        {
          src: "picsum.photos/200/300?random=10",
          alt: "mosaic collection image",
        },
        {
          src: "picsum.photos/200/300?random=11",
          alt: "mosaic collection image",
        },
      ],
    };
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
}

.glow {
  display: flex;
  align-items: flex-end;
  color: #ffffff;
  text-shadow: 0 0 10px rgb(255, 246, 121),
    0 0 20px rgba(255, 255, 255, 0.5),
    0 0 30px rgba(255, 255, 255, 0.3);
  font-size: 2em;
  letter-spacing: 3px;
  cursor: pointer;
  top: 0;

}
.carPos{
  width: 100%;
  
}
a {
  color: white;
}
</style>

<script>

export default {
  name: 'UserCard',
  props: {
    information: Object,
    photo: ImageData,
  }
}

</script> 



<template>
  <div class="card">
    <div class="picture">
      <img :src="require(`@/assets/${information.photo}`)" alt="">
    </div>
    <div class="zone_txt">
      <div>
        <h2>{{ information.titre }}</h2>
        <p>{{ information.description }}</p>
      </div>
      <div>
        <hr>
        <a :href="information.lien" target="_blank">Accès Github</a>
      </div>
    </div>
  </div>
</template>

<style scoped>
h2{
  padding-left: 2px;
}

.card{
  display: flex;
  flex-wrap: wrap;
  background-color: rgba(47, 218, 183, .6);

  width: 50%;
  margin: 2vh;
  padding: 2vh;
}

.picture{
  display: flex;
  justify-content:center;
}

.zone_txt{
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

</style>

<!-- <template>
  <div>
    <vue3-carousel :options="carouselOptions">
      <vue3-carousel-slide v-for="item in items" :key="item.id">
        <!- - Votre contenu de diapositive ici -- >
        <div>{{ item.content }}</div>
      </vue3-carousel-slide>
    </vue3-carousel>
  </div>
</template>

<script>
import { ref } from 'vue';
import Vue3Carousel from 'vue3-carousel';

export default {
  components: {
    Vue3Carousel,
    Vue3CarouselSlide,
  },
  data() {
    return {
      items: [
        { id: 1, content: 'Slide 1' },
        { id: 2, content: 'Slide 2' },
        { id: 3, content: 'Slide 3' },
      ],
      carouselOptions: {
        // Options du carousel (consultez la documentation de vue3-carousel)
      },
    };
  },
};
</script> -->

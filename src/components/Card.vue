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
        <h2 class="titre_card"><b>{{ information.titre }}</b></h2>
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
  background-color: #d9d4e7;

  width: 40%;
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

a{
  text-decoration: underline;
}

.titre_card{
  color: #0e172c;
}

</style>

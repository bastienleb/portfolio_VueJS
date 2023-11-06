<script>
export default {
  name: 'ContactMe',
  props: {
    msg: String,
  }
}
</script>

<template>
  <div class="navbar">
    <h1>
      Bastien LEBLET
    </h1>
    <p v-if="msg">{{ msg}}</p>
    <div class="lien">
      <a href="#">Réalisation</a>
      <a href="#">CV</a>
      <a href="#">Me contacter</a>
    </div>
  </div>
</template>

<style scoped>
  .navbar{
    position: fixed;
    top: 0;
    width: 100%;

    display: flex;
    justify-content: space-between;
    padding: 2.5vh 0;

    background-color: rgba(112,170,225,0.5) ;
  }

  .lien{
    flex-wrap: wrap-reverse;
  }

  h1{
    margin: 0 1vh;
  }

  a{
    margin: 0 5vh ;
  }
</style>
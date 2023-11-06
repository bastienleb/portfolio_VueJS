<template>
  <Navbar msg=""/>
<!--  <img alt="Vue logo" src="./assets/logo.png" >-->
  <div class="component">
  <h1 class="gros_titre">Réalisation</h1>
    <div v-for="user in users" :key="user.id" >
      <h1>{{ user.langage }}</h1>
      <div class="all_card">
        <Card v-for="info in user.information" :key="info.id" :information ="info"/>
      </div>
    </div>
  </div>

  <Footer/>
</template>

<script>

import Navbar from "@/components/Navbar.vue";
import Card from "@/components/Card.vue";
import Footer from "@/components/Footer.vue";

import Data from "@/assets/data.json"
export default {
  name: 'App',
  components: {
    Navbar,
    Card,
    Footer
  },
  data(){
    return { users: Data }
  }
}
</script>


<style>

</style>


<script>
export default {
  name: 'UserFooter',
  props: {
    msg: String,
  }
}
</script>

<template>
  <div class="footer">
    <div class="all_info">
      <p>Bastien LEBLET</p>
      <p>bastienleblet@gmail.com</p>
    </div>
    <div class="all_icon">
      <a href="https://www.linkedin.com/in/leblet-bastien/" target="_blank"><img class="icon" src="../assets/linkedin.png" alt="logo linkedin"></a>
      <a href="https://github.com/bastienleb" target="_blank"><img class="icon" src="../assets/github.png" alt="logo github"></a>
    </div>
  </div>
</template>

<style scoped>
  .footer{
    background: rgba(198, 186, 231,.4) ;
    padding: 1vh 0;
    display: flex;
    justify-content: space-between;
  }

  .all_icon{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    width: 4.5%;
    margin-right: 2vh;
  }

  .all_info{
    padding-left: 10px;
  }

</style>
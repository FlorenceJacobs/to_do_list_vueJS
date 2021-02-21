<template>
  <div>
    <div class="header">Workshop : "To do List" with Vue.js</div>
    <div class="imageHeader"><img src="../.././public/logo_vue.png" alt="logovuejs"></div>
  </div>
</template>

<script>
export default {
  name: 'HeaderList',
  data(){
      return {

      }
  }
}

</script>


<style scoped>
  .header {
    background-color: #34495e;
    width: 100%;
    min-height: 5rem;
    text-align: center;
    line-height: 5rem;
    font-size: 1.5rem;
    color : white;
  }
  img {
    position : absolute;
    top : 0px;
  }

</style>
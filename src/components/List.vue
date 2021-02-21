<template>
  <div>
    <div class="h4 mt-4">
      My "To Do List" :
    </div>
    <ul>
      <li v-for="(element, index) in listElement" v-bind:key="index">
        <div class="card mt-2">
          <div class="card-body">
            {{ element }}
            <div v-on:click="deleteElement([index])" class="btn">X</div>
          </div>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'List',
  data(){
    return {

    }
  },
  methods: {
    deleteElement: function(index){
      this.listElement.splice(index, 1);
    }
  },
  props: ['listElement']

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  li, ul {
    padding : 0;
    margin:0;
    list-style-type : none;
  }
  .btn{
    position : absolute;
    top : 13px;
    right : 13px;
    background-color: #41b783;
  }
</style>

<template>
  <body>
    <headerList></headerList>
    <div class="container mt-5">
      <div class="row">
        <div class="col-md-5 m-auto">
          <h1 class="text-center">TO DO or not TO DO ?</h1>
          <h2 class="h4 mt-4 text-center">Things I should do...One day.</h2>
          <div class="form-group mt-5">
            <label for="list" class="h5">Add to my list :</label>
            <input v-on:keyup.enter="addElement" type="text" class="form-control" id="list" placeholder="Type something to do">
            <!-- OR : input v-model="newElement.element" (in data) And then button v-on:click="push in array"-->
          </div>
          <list v-bind:listElement="listElement"></list>
        </div>
      </div>
    </div>
  </body>  
</template>

<script>
import HeaderList from './components/HeaderList.vue'
import List from './components/List.vue'

export default {
  name: 'App',
  components: {
    'list' : List,
    'headerList' : HeaderList,
  },
  data() {
    return {
      element : "",
      listElement : ["Task added. Try to delete it -->"],
    }
  },
  methods: {
    addElement : function(e) {
      this.element = e.target.value;
      this.listElement.push(this.element);
      e.target.value = "";
    }

  }
}
</script>

<style>
body {
  background-color: #9cdcc4;
  height: 100vh;
}
</style>

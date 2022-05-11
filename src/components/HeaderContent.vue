<template>
  <header>
    <h1>Boolflix</h1>
    <div class="input-group mb-3">
  <input type="text" class="form-control"  v-model="search" placeholder="movie name" aria-label="movie name" aria-describedby="button-addon2">
  <button class="btn btn-outline-secondary" @click="ricerca">Inizia Ricerca</button>
</div>

    <!--<input type="text" v-model="search" @keyup.enter="ricerca" >
    <button @click="ricerca">Inizia Ricerca</button>-->
  </header>
</template>

<script>

export default {
  name: 'HeaderContent',
  data(){
    return{
      search:''

    }
  },
  methods:{
    ricerca(){
      this.$emit('goSearch', this.search),
      this.search=''
    }
  }
  
}
</script>

<style lang="scss">
header{
  height:100px;
  background-color:rgb(28, 27, 27);
}
h1{
  color:red;
  font-size:30px;
  font-family:'Roboto Condensed';
  padding-top:5px;
  padding-left:8px;
}
.input-group{
color:white;
padding-left:10px;
}

</style>

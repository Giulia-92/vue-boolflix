<template>
<main>
  <div id="app">
    <HeaderContent @goSearch="search" />
    <div class="sfondo">
      <card-content :items="movies" title='Movies' />
    </div>
     <card-content :items="series" title='Series' />
  </div>
  </main>
</template>

<script>
import HeaderContent from './components/HeaderContent.vue'
import axios from 'axios'
import CardContent from './components/CardContent.vue';
export default {
  name: 'App',
  components: {
   HeaderContent,
    CardContent
  },
  data(){
    return{
      apiKey:'b1114bdb80acbfdef0b6a3f26eab00e2',
      apiPath:'https://api.themoviedb.org/3/search/',
      series:[],
      movies:[],
    }
  },
  methods:{
    toMovies(queryParams){
      axios.get(this.apiPath +'movie',queryParams).then((res)=>{
        this.movies=res.data.results;
      })
    },
    
   
    search(text){
      const queryParams={
        params:{
          api_key:this.apiKey,
          query:text
        }
      }
      console.log(queryParams)
      this.toMovies(queryParams)
      
    }
    
  }
}
</script>

<style lang="scss">
main{
  background-color: rgb(44, 42, 42);
  height:100%;
}

</style>

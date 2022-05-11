<template>
  <div>
    <input type="text" v-model="search" @keyup.enter="$emit('goSearch',search)">
    <button @click="ricerca">Inizia Ricerca</button>
  </div>
</template>

<script>
import state from'../store.js'
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


*created(){
       console.log(this.apiPath)
      axios.get(this.apiPath).then((res)=>{
          this.filmList =res.data.results
          console.log (res.data.results) 
      })   
  },*

"id": 105,
            "original_language": "en",
            "original_title": "Back to the Future",
            "overview":

<style scoped lang="scss">

</style>

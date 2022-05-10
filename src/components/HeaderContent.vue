<template>
  <div>
    <ul>
      <li v-for="(item) in filmList" :key="item"> :img="item.poster_path :id="item.id" :linguage="item.original_linguage" :title="item.original_title"/>
      </li>
    </ul>
    
  </div>
</template>

<script>
import axios from 'axios';
export default {
  name: 'HeaderContent',
  props: {
    id: Number,
    linguage:String,
    title:String,
     img:String,
  },
  data(){
    return{
      filmList:[],
      apiPath:'https://api.themoviedb.org/3/search/movie?api_key=b1114bdb80acbfdef0b6a3f26eab00e2&query=ritorno+al+futuro'
    }
  },
  created(){
       console.log(this.apiPath)
      axios.get(this.apiPath).then((res)=>{
          this.cardList =res.data.response
          console.log (res.data.response) 
      })   
  },
}
</script>




"id": 105,
            "original_language": "en",
            "original_title": "Back to the Future",
            "overview":
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>

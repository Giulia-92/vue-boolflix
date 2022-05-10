<template>
  <div>
    <ul>
      <li>{{id}}</li>
      <li>{{linguage}}</li>
      <li>{{title}}</li>
      <li>{{  }}</li>
      <li>{{  }}</li>
    </ul>
    
  </div>
</template>

<script>
export default {
  name: 'HeaderContent',
  props: {
    id: Number,
    linguage:String,
    title:String
  },
  data(){
    return{
      apiPath:'https://api.themoviedb.org/3/search/movie?api_key=b1114bdb80acbfdef0b6a3f26eab00e2&query=ritorno+al+futuro'
    }
  },
  created(){
       console.log(this.apiPath)
      
  }
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

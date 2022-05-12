<template>
<div class="container">
        <h3 class="titoli">{{title}}</h3>
        <div class="row">
    <div v-for="(item) in items" :key="item.id" class="col-6 col-md-4 col-lg-3 mb-2">
        <div class="card mt-5" style="width: 16rem;">
            <img :src="imagePath+item.poster_path" class="card-img-top" alt="poster">
                <div class="card-body center">
                    <h1 class="card-title text white center fw bold my-3">titolo:{{item.title ? item.title : item.name}}</h1> 
                    <p class="card-text"> voto:{{item.vote_average}}
                        <br /> id:{{item.id}},
                        <br />
                        lingua: <img class="bandiera" v-if="item.original_language ==='it'" :src="require('../assets/style/'+item.original_language+'.png')" alt="italiano">,
                        <br />
                        lingua: <img class="bandiera" v-if="item.original_language ==='en'" :src="require('../assets/style/'+item.original_language+'.png')" alt="inglese"></p>
                </div>
        </div>
    </div>
</div>














            <!--<div v-for="(item) in items" :key="item.id" class="col-6 col-md-4 col-lg-3 mb-3">
                 <img :src="imagePath+item.poster_path" alt="">
                id:{{item.id}},
                <br />
                voto:{{item.vote_average}}
                <br />
                titolo originale:{{item.original_title ? item.original_title:item.original_name}},
                <br />
                titolo:{{item.title ? item.title : item.name}},
                <br />
                lingua: <img class="bandiera" v-if="item.original_language ==='it'" :src="require('../assets/style/'+item.original_language+'.png')" alt="italiano">
                lingua: <img v-if="item.original_language ==='en'" :src="require('../assets/style/'+item.original_language+'.jpg')" alt="inglese">
                
            </div>-->
        </div>
  
</template>
<script>
export default {
        name:'CardContent',
        props:{
            items:Array,
            title:String,
        },
        data(){
            return{
                imagePath:'https://image.tmdb.org/t/p/w342'
            }
        },
       
        
    
}
</script>
<style lang="scss">
main{
   background-color:rgb(40, 38, 38);
    width:100%;  
}


.bandiera{
    height:15px;
    width:25px;
}
.titoli{
    display: flex;
    justify-content: center;
    font-size:50px;
    color: white;
    margin-top:8px;
}

</style>










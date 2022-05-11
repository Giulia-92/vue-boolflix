<template>
    <div class="container">
        <h3>{{title}}</h3>
        <ul class="row">
            <li v-for="(item) in items" :key="item.id" class="col-6 col-md-4 col-lg-3 mb-3">
                id:{{item.id}},
                <br />
                voto:{{item.vote_average}}
                <br />
                titolo originale:{{item.original_title ? item.original_title:item.original_name}},
                <br />
                titolo:{{item.title ? item.title : item.name}},
                <br />
                lingua:{{item.original_language}} <br />
                <!--<img :src="require('../assets/style/bandiera' +item.original_language+'png')" alt="">-->
            </li>
        </ul>
    </div>
</template>
<script>
export default {
        name:'CardContent',
        props:{
            items:Array,
            title:String,
        },
        
    
}
</script>
<style lang="scss">
.container{
    
    color: white;
    font-family:'Roboto Condensed';
    width: 100%;


}
</style>
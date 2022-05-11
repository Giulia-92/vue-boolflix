<template>
    <div>
        <h1>{{title}}</h1>
        <ul>
            <li v-for="(item) in items" :key="item.id">
                id:{{item.id}},
                voto:{{item.vote_average}}
                titolo originale:{{item.original_title ? item.original_title:item.original_name}},
                titolo:{{item.title ? item.title : item.name}},
                lingua:{{item.vote_average}}
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
        data(){
            return
        },
    
}
</script>
<style lang="scss">

</style>
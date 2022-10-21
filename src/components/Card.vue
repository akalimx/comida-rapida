<template>
    <div class="col col-3 p-2 col-sm">
    <img :src="url" :alt="nombre">
    <h2 class="mt-1">¡{{ nombre }}!</h2>
    <p>{{descripcion}}</p>
    <a class="btn btn-warning" target="_blank" :href="ordenar">Ver más</a>
    </div>
</template>
<script>
export default{
props:{
    url:{
        String,
    },
    nombre:{
        String,
    },
    descripcion:{
        String,
    },
    ordenar:{
        String,
    }
},
};
</script>
<style scoped>
div{
box-shadow: 0px 0px 10px rgb(145, 145, 253);
text-align: center;
width: 30vw;
margin: 20px;
box-sizing: border-box;
border-radius: 10px;
}
a{
text-decoration: none;
margin-bottom: 10px;
}
div:hover{
transform: scale(1.05,1.05);
    transition: 80ms;
}
div>img{
width: 300px;
border-radius: 5px; 
margin-top: 9px;
}
@media screen and (max-width:900px) {
div>img{
    width: 20vw;
}
}
@media screen and (max-width:1000px) {
div>img{
    width: 25vw;
}
}
</style>
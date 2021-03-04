<template>
    <div class="block-container">
        <h3>{{title}}</h3>
    </div>
</template>

<script>
export default {
    name:'TitleComponent',
    props:{
        title:String
    }
}
</script>

<style scoped>
.block-container
{
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    padding: 5% 5%;
    background: black;
    margin-bottom: 4%;
}
h3
{
margin: 0;
font-size: 22px;
}
</style>
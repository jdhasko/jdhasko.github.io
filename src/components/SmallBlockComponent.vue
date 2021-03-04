<template>
    <div class="main-container">
        <div class="flex-container">
        <div class="text-container"> 
            <h4>{{title}}</h4>
            <h5>{{subTitle}}</h5>
        </div>

        <template v-if="buttonData.hasButton===true">
            <div class="button-box">
            <MyButton :text='buttonData.text' :icon="buttonData.icon" :link="buttonData.link"/>
            </div>
        </template>
        </div>
    </div>
</template>

<script>
import MyButton from './MyButton'

export default {
    name:'SmallBlockComponent',
    components:{MyButton},
    props:
    {
        title:String,
        subTitle:String,
        buttonData:Object
    }
}
</script>

<style scoped>

    h4,h5
    {
        text-align: left;
        margin:0;
        font-weight: normal;
    }
    h4
    {
        font-size: 20px;
        font-weight: bold;
    }
    .main-container
    {
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        background-color: black;
        padding: 4%;
        margin-bottom: 5%;
        text-align: center;
    }
    .flex-container
     {
        width: 100%;
        justify-content: space-between; 
    }
    
    .text-container
    {
    }
    .button-box{
      
    min-width: 165px;
    }
</style>
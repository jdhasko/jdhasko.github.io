<template>
    <div class="main-container">
       <div class="flex-header">
           <template v-if="logo != '' ">
            <img :src="require(`@/assets/${logo}`)"   alt="netto-icon">
           </template>
       <div class="block-display">
           <h4>{{title}}</h4>
           <h5>{{subTitle}}</h5>
       </div>
       </div>
       <div class="bottom-container">
        <p>{{description}}</p>
       </div>
       <template v-if="buttonData.hasButton===true">
       <MyButton :text='buttonData.text' :icon="buttonData.icon" :link="buttonData.link"/>
       </template>
    </div>
</template>

<script>
    import MyButton from './MyButton'


export default {
    name:'PositionComponent',
    components:
    {
        MyButton
    },
    props:
    {
        logo:String,
        title:String,
        subTitle:String,
        description:String,
        buttonData:Object
    }
}
</script>

<style scoped>
    .main-container
    {
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        background-color: black;
        padding-bottom: 3%;
        margin-bottom: 5%;
    }

    .flex-header
    {
        display: flex;
        padding-top: 5%;
        padding-left:5%;
        padding-right:5%;
    }
    .flex-header > img
    {
        padding-right:2.5%;
        width: 70px;
        height: 70px;
    }

    .block-display
    {
        
        display: block;
    }
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
    .bottom-container > p
    {
        text-align: justify;
        padding:0px 5%;
    }
</style>
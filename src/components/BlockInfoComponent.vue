<template>
    <div id="block-container">
        <h3>{{Title}}</h3>
        <div>
            <div v-for="item in ListItemData" :key="item">
            <ListItem :topic="item.topic" :data="item.data" :oneline="item.oneline" :marginSize="MarginSize"/>
            </div>
        </div>
        <template v-if="buttonData.hasButton===true">
        <div class="button-box">
        <MyButton :text="buttonData.text" :icon="buttonData.icon" :link="buttonData.link"/>
        </div>
        </template>
    </div>
</template>

<script>
import ListItem from './ListItem'
import MyButton from './MyButton'

export default {
    name:'BlockInfoComponent',
    props:
    {
        Title:String,
        ListItemData:[Object],
        buttonData:Object,
        MarginSize:Number
    },
    components:
    {
        ListItem,
        MyButton
    }
}
</script>

<style scoped>
#block-container
{
   font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    text-align: left;
    background-color:black;
    width: 49%;
    padding-bottom: 3%;
    padding-top:3%;
    margin-bottom: 4%;
}
h3
{
    font-size: 28px;
    text-align: left;
    padding-left: 8%;
    margin: 2% 0%;
}
    .button-box
    {
        margin-top: 3%;
    }

       /**   MOBILE VIEW */
   
   @media only screen and (max-width:820px)
   {
    #block-container
    {
        width: 100%;
    }
    h3
    {
        font-size: 25px;
    }
   }
</style>
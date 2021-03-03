<template>
    <div id="block-container">
        <h3>{{Title}}</h3>
        <div>
            <div v-for="item in ListItemData" :key="item">
            <ListItem :topic="item.topic" :data="item.data" :oneline="item.oneline" :marginSize="MarginSize"/>
            </div>
        </div>
        <template v-if="buttonData.hasButton===true">
        <MyButton :text="buttonData.text" :icon="buttonData.icon" :link="buttonData.link"/>
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
    padding-bottom: 2%;
}
h3
{
    font-size: 28px;
    text-align: left;
    padding-left: 8%;
    margin: 2% 0%;
}

</style>
<template>
<div class="flex-box">
  <div id="titles-container">
     <p :style="cssVars" id="topic"> {{topic}} </p>
  </div>

  <div id="data-container">
         <div v-if="oneline === 0">
          <div v-for="line in data" :key="line">
             <p :style="cssVars" id="data">{{line}}</p>
          </div>
        </div>

        <div v-else> 
              <p :style="cssVars" id="data">{{data}}</p>
         </div> 
  </div>
</div>
</template>

<script>
export default {
    name:'ListItem',
    props:
    {

        topic:String,
        data:Object,
        oneline:Number,
        marginSize:Number
    },
    computed: {
      cssVars() {
        return {
          'margin-top': this.marginSize +"px",
          'margin-bottom': this.marginSize +"px"
        }
    }}
}
</script>

<style scoped>
.flex-box
{
        display: flex;
        justify-content: space-between;
        width: 78%;
        margin: auto;

}
#topic
{
    font-size: 16px;
}
#data
{
    text-align: right;
    font-size: 16px;
    font-weight: bolder;
}
</style>
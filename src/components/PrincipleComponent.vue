<template>
    <div class="principle-container">
        <template v-if="isReversed===false">
            <div class="flex-box">
                <img :src="require(`@/assets/${img}`)">
                <div class="vertical-aligner">
                    <div class="content-box">
                        <div class="padding">
                    <template v-if="quote===true">
                            <h3><q>{{title}}</q></h3> 
                            <p class="auth">{{content}}</p>
                    </template>
                    <template v-else>
                        <h3>{{title}}</h3> 
                        <p>{{content}}</p>
                    </template>
                        </div>
                    </div>
                </div>
            </div>
        </template>

        <template v-if="isReversed===true">
            <div class="flex-box">
                <div class="vertical-aligner">
                    <div class="content-box">
                        <div class="padding-rev">
                    <template v-if="quote===true">
                            <h3><q>{{title}}</q></h3> 
                            <p class="auth">{{content}}</p>
                    </template>
                    <template v-else>
                        <h3>{{title}}</h3> 
                        <p>{{content}}</p>
                    </template>
                        </div>
                    </div>
                </div>
                 <img id="img-reverse" :src="require(`@/assets/${img}`)">
            </div>
        </template>
    </div>
</template>

<script>
export default {
    name:'PrincipleComponent',
    props:
    {
        title:String,
        content:String,
        img:String,
        quote:Boolean,
        isReversed:Boolean
    }
}
</script>

<style scoped>
.principle-container
{   
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin:auto;
    width: 65%; 
    margin-bottom: 3.5%
}
.vertical-aligner
{
    margin: auto;
    width: 100%;
}
.flex-box
{
    display:flex;
}
.padding
{
    padding: 1% 2.6%;
}
.padding-rev{
        padding: 1% 2.6%;
    width: 85%;
}

.content-box
{
    background: black;
    padding: 2% 1%;
    width: 100%;
    min-height: 155px;
    max-height: 240px;
    overflow: hidden;
    
}

.principle-container img
{
    margin-left: -7%;
    height: 250px;
    width: 250px;
}

h3, p
{
    text-align: left;
    margin: 1% 3%;
}
p
{
    text-align: justify;
}
h3
{
    font-size: 30px;
}
.auth
{
    text-align: right;
    padding-bottom: 2%;
}
#img-reverse
{
        margin-right:-7%;
 
}

q
{
    font-size: 25px;
}

@media screen and (max-width:820px) {
    .flex-box{
        flex-direction: column;
    }

.principle-container img
    {
       margin-bottom:-15%;
       height: 125px;
       width: 125px;
    }
    #img-reverse
    {
        margin:auto;
        margin-right: -7%;
        margin-top:-15% 
    }
    img{
        z-index: 2;
    }
    p{
    text-align: justify;
    }
    h3{
    font-size: 18px;
    }
    q
    {
        font-size: 18px;
    }
    .padding
    {
        padding-top:15%;
    }
    .content-box
    {
        height: auto;
        max-height: none;
    }
    .padding-rev
    {
        width: auto;
        padding-top:none;
        padding-bottom: 15%;
        padding-top:3%;
    }
    .principle-container
   {
       margin-bottom:1.5%;
   }
}

</style>
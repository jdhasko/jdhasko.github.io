<template>
    <div id="button-container"  @click="onClick">
            <button>
                <div id="logo"> {{icon}} </div> {{text}}
            </button>
    </div>
</template>
<script>
export default {
    name:'MyButton',
    props:
    {   
        icon:String,
        text:String,
        link:String
    },
    methods:
    {
        onClick: function()
        {
            window.location.href = this.link;
        }
    }
}
</script>

<style scoped>
   #button-container > button
    {
        margin: auto;
        text-align: center;
        font-size: 15px;
        padding: 10px 25px;
        color: white;
        background: #5c19da;
        border: none;
    }
       #button-container > button:hover
    {

        background: #4000b6;

    }
    #logo{
        font-family: "Segoe MDL2 Assets";
        display: inline;
        padding: 5px;
        font-weight: bold;
    }
    #button-container >button:focus
    {
        outline: none;
    }

    #button-container
    {
        padding-top: 25px;
        width: 100%;
    }
    a:link,a:visited,a
    {
    text-decoration: none;
    }

</style>
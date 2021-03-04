<template>
    <div id="profile-container">
        <div id="profile-flex"> 
        <div class="profile-item">
            <img id="profile_pic" src="../assets/me_1.jpg" height="300" width="300" alt="A picture of the author">
        </div>
        <div id="welcome-container" class="profile-item">
            <h2>Hey there,</h2>
            <h3>My name is Dominik</h3>
            <h4>and I am a front-end developer and a student in Computer Science.</h4>
        
            <MyButton text="view projects" icon="&#xE72D;"/>

        
        </div>
        </div>
        <div id="about_me" class="profile-item">
            <h3>ABOUT ME</h3>
            <p>
                I am a 20 years old student at Zealand Academy in Computer Science with a great desire for programming. I am a talkative, creative and open-minded person. I was born and raised in Hungary, but when I turned 18, I moved to Denmark to take my education in Denmark. Besides my studies I also learn Danish, as I find it interesting just like the Danish way of living and culture. In my free time I love cooking, playing the piano and I am always open for a coffee and a great conversation.
                If you would like to know more about my way of thinking click here.
            </p>
        </div>

    </div >
</template>

<script>
import MyButton from "./MyButton"
export default {
    name:'ProfileComponent',
    components:{MyButton}
    
}
</script>

<style scoped>
    #profile-container{
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        background: black;


        width: 78%;
        margin:auto;
        margin-top: 80px;
        margin-bottom:5% ;
    }
    #profile-flex
    {
        display: flex;
        position: relative;
        text-align: left;
    }
    #profile_pic
    {
        margin-left: -25px;
        margin-top: -25px;
    }
    #about_me
    {
          grid-column: 1 / 3;
    }


    #welcome-container
    {
        padding: 45px 25px 30px 55px;
        width: 100%;
            }
    #welcome-container > h2
    {
        font-size: 55px;
        letter-spacing: 5px;
        margin: 0;
    }
    #welcome-container >h3
    {
        margin:0;
        margin-top: 10px ;
        font-size:35px;
        letter-spacing: 3px;
        font-weight: 300;
    }
        #welcome-container >h4
    {
        margin: 0;
        margin-top: 0px ;
        font-size:20px;
        letter-spacing: 1px;
        font-weight: 300;
    }

 

    #about_me >h3
    {
        text-align: left;
        font-size: 33px;
        margin: 0;
        margin-left: 10%;
        margin-top: 15px;
    }
    #about_me > p
    {
        padding: 0 13% 4%  ;
        text-align: justify ;
    }


</style>
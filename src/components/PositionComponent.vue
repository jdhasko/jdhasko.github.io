<template>
    <div class="main-container">
       <div class="flex-header"> <img src="../assets/netto-logo.png"   alt="netto-icon">
       <div class="block-display">
           <h4>Csöcsök és segg a kurva élet</h4>
           <h5>2015-0214</h5>
       </div>
       </div>
       <div class="bottom-container">
        <p>After a few months in Netto, I got promoted to a First Assistant.
I've been working at multiple stores around Zealand and I felt like,
despite the fact that I'm not a Dane, my work was more than appreciated all the time. Danish people are very supportive and encouraging. Since this period started, I became responsible for a store and for a team, therefore I gained experience in team-leading, and my time-management skill significantly improved.</p>
       </div>
    </div>
</template>

<script>
export default {
    name:'PositionComponent'
}
</script>

<style scoped>
    .main-container
    {
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        background-color: black;
        padding-bottom: 3%;

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
        width: 70px;
        height: 70px;
    }

    .block-display
    {
        padding-left: 3%;
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
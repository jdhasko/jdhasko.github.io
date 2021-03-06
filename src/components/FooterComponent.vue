<template>
    <div class="flex-box">
        <p>Made with <i class="fas fa-heart fa-sm"></i> by János Dominik Haskó</p>
        <p>dominikjanoshasko@gmail.com</p>
        <p>Powered by <i class="fab fa-vuejs fa-lg"></i> vue.js</p>
    </div>
</template>

<script>
export default {
    name:'FooterComponent',

}
</script>

<style scoped>
.flex-box
{
    width: 100%;
    background: black;
    display: flex;
    justify-content: space-evenly;
    font-size: 14px;
}
.fa-heart
{
    color:red;
}
.fa-vuejs
{
    color:#41b783;
}

@media screen and (max-width: 820px) {
    .flex-box
    {
        flex-direction: column;
    }
    p
    {
        margin: 3px 0;
    }
}
</style>
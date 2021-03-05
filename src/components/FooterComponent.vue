<template>
    <div class="flex-box">
        <p>Made with <i class="fas fa-heart fa-sm"></i> by János Dominik Haskó</p>
        <p>dominikjanoshasko@gmail.com</p>
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
</style>
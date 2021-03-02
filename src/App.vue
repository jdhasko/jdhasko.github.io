<template>
  <HeaderComponent/>
  <HomeComponent/>
</template>

<script>
import HomeComponent from './components/HomeComponent.vue'
import HeaderComponent from './components/HeaderComponent.vue'

export default {
  name: 'App',
  components: {
    HomeComponent,
    HeaderComponent
  }
}
</script>

<style>
#app {
  font-family: 'Courier New', Courier, monospace;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color:white;
  background-color:  #5c19da;
    height: auto;

}
body
{
  margin: 0;
  height: auto;
}
html
{
  height: auto;
}
</style>

<template>
  <header>
    <a href="#Home"><img class="logo" width="55px" height="55px" src="../assets/logo.png"></a>
    <ul>
    <li><a href="#Home">&lt;home/&gt;</a></li>
    <li><a target="_blankS" href="https://github.com/jdhasko?tab=repositories">&lt;my_Projects/&gt;</a></li>
    <li><a target="_blanks" href="cv.pdf">&lt;resume_CV/&gt;</a></li>
    <li><a href="#contact">&lt;contact/&gt;</a></li>
  </ul>
  </header>
</template>

<script>
export default {
  name: 'HeaderComponent',
}
</script>

<style scoped>
header{
    position: fixed;
    top:0;
    left: 0;
    width: 100%;
    justify-content: space-between;
    align-items: center;
    transition: 0.6ms;
    display: flex;
    height: 8vh;
    z-index: 1;
    background: black;
  }

  header ul
  {
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;

  }
  header ul li 
  {
    position: relative;
    list-style: none;
        margin: 0px 10px;

  }

    header ul li:hover
  {
    background: rgb(165, 165, 165);
  }

  header ul li a
  {
    position: relative;
    text-decoration: none;
    color: white;
    padding: 15px 10px;
  }

  header .logo{
    width: 55px;
    height: 55px;
    position: relative;
    transition: 0.6ms;
    margin-left: 0,15% ;
  }

</style>
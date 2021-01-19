<template>
  <Section> 
      <div id="Home"> 
                <div class="caption">
                <span class="border">&lt;Welcome to the future./&gt;</span>
                </div>
      </div>

      <div id="button-container">     
           <button v-on:click="menuChange('Profile')" >&lt;about_me/&gt;</button>
           <button v-on:click="menuChange('Principles')" >&lt;my_principles/&gt;</button>
      </div>

      <template v-if="menu=='Profile'">
          <p>asdasdasd</p>
      </template>
    
  </Section>
</template>


<script>
export default {
  name: 'HomeComponent',
  data() {
      return{
      menu : "None"
      }
  },
  methods:
  {
      menuChange: function(menuOption)
      {
          this.menu = menuOption;
          console.log("The menu has been changed to: " + this.menu);
      }
  }
}
</script>

<style>
    #Home
    {
        background-image: url("../assets/main-background.gif");
        height: 85vh;
    }
    .caption 
    {
        position: absolute;
        left: 0;
        top: 35%;
        width: 100%;
        text-align: center;
        color: white;
        font-size: 23px;
        letter-spacing: 8px;
    }

    .border
    {
        padding: 10px 45px;
        background: black;
    }

    #button-container 
    {
        display: flex;
        justify-content: space-around;
        width: 100%;
        height: auto;
    }

    #button-container button 
    {
        font-family: 'Courier New', Courier, monospace;
        width: 50%;
        height: 5vh;
        background: black;
        color: white;
        border: none;
    }

    #button-container button:hover
    {
        background:rgb(165, 165, 165);
    }

    #button-container button:focus
    {
        background: #5c19da;
        outline: none;
    }
    
</style>
<template>
    <div>
      <div id="Home"> 
                <div class="caption">
                <span class="border">&lt;Welcome to the future./&gt;</span>
                </div>
      </div>

      <div id="button-container">     
           <button class="selector-button" v-on:click="menuChange('Profile')" v-bind:class="{purple : ( menu == 'Profile') }">&lt;about_me/&gt;  </button>
           <button class="selector-button" v-on:click="menuChange('Principles')" v-bind:class="{purple : ( menu=='Principles')}">&lt;my_principles/&gt;</button>
      </div>

      <template v-if="menu=='Profile'">
          <ProfileComponent/>
      </template>
    
  </div>
</template>


<script>
import ProfileComponent from './ProfileComponent'


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
  },
  components:
  {
      ProfileComponent
  }
}
</script>

<style>
    #Home
    {
        background-image: url("../assets/main-background.gif");
        height: 95vh;
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

    .selector-button 
    {
        font-family: 'Courier New', Courier, monospace;
        width: 50%;
        height: 5vh;
        background: black;
        color: white;
        border: none;
    }

    .selector-button:hover
    {
        background:rgb(41, 41, 41);
    }

    .selector-button:focus
    {
        outline: none;
    }

    .purple 
    {
        background: #5c19da;
    }
    .purple:hover 
    {
        background: #5c19da;
    }
</style>
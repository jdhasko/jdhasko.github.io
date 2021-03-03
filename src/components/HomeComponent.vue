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
          <div class="flex-container">
          <BlockInfoComponent 
          Title="PERSONAL INFORMATION" 
             MarginSize=16
           :ListItemData="[
           {topic: 'FULL NAME', data:'János Dominik Haskó', oneline:1},
           {topic: 'D.O.B.', data:'November 2000', oneline:1},
           {topic: 'ADDRESS', data:'Roskilde - Denmark', oneline:1},
           {topic: 'EMAIL', data:'dominikjanoshasko@gmail.com', oneline:1},
           {topic: 'LANGUAGES', data:['English - Professional','Hungarian   - Native', 'Danish - Beginner'], oneline:0}]"
           :buttonData="{icon: '&#xE896;', text: 'download resume   ', link: 'https://github.com/jdhasko', hasButton:true}" />

          <BlockInfoComponent 
          Title="EXPERIENCE" 
          MarginSize=7
           :ListItemData="[
           {topic: 'PROGRAMMING LANGUAGES', data:['Javascript, Typescript','HTML, CSS','C#','SQL', 'React', 'Vue'], oneline:0},
           {topic: 'METHODOLOGIES', data:['Agile Developent', 'XP and SCRUM'], oneline:0},
           {topic: 'OTHER', data:['UI Design - Prototyping','Adobe Ps, Pr, Xd etc.', 'Computer Networks'], oneline:0}]"
           :buttonData="{icon: '&#xE890;', text: 'view grades ', link: '', hasButton:true}" />
          </div>
      </template>
    
  </div>
</template>


<script>
import ProfileComponent from './ProfileComponent'
import BlockInfoComponent from './BlockInfoComponent'

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
      BlockInfoComponent,
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

    .flex-container
    {
        display: flex;
        justify-content: space-between;
        width: 78%;
        margin: auto;
    }

</style>
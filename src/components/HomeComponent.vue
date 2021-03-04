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

                <div class="background-container">
                    <div class="flex-container">
                        <BlockInfoComponent 
                        Title="PERSONAL INFORMATION" 
                        MarginSize='16'
                        :ListItemData="[
                        {topic: 'FULL NAME', data:'János Dominik Haskó', oneline:1},
                        {topic: 'D.O.B.', data:'November 2000', oneline:1},
                        {topic: 'ADDRESS', data:'Roskilde - Denmark', oneline:1},
                        {topic: 'EMAIL', data:'dominikjanoshasko@gmail.com', oneline:1},
                        {topic: 'LANGUAGES', data:['English - Professional','Hungarian   - Native', 'Danish - Beginner'], oneline:0}]"
                        :buttonData="{icon: '&#xE896;', text: 'download resume   ', link: 'https://github.com/jdhasko', hasButton:true}" />

                        <BlockInfoComponent 
                        Title="EXPERIENCE" 
                        MarginSize='7'
                        :ListItemData="[
                        {topic: 'PROGRAMMING LANGUAGES', data:['Javascript, Typescript','HTML, CSS','C#','SQL', 'React', 'Vue'], oneline:0},
                        {topic: 'METHODOLOGIES', data:['Agile Developent', 'XP and SCRUM'], oneline:0},
                        {topic: 'OTHER', data:['UI Design - Prototyping','Adobe Ps, Pr, Xd etc.', 'Computer Networks'], oneline:0}]"
                        :buttonData="{icon: '&#xE890;', text: 'view grades ', link: '', hasButton:true}" />
                    </div>
                </div>


    <div class="extra-container">
    <div class="flex-container">
            <div class ="flex-vertical">
                <TitleComponent title='WORK EXPERIENCE'/>
                <PositionComponent
                logo="netto-logo.png"
                title="NETTO - Leader Assistant"
                subTitle="2020 July - Present"
                description = "After a few months in Netto, I got promoted to a First Assistant.
I've been working at multiple stores around Zealand and I felt like,
despite the fact that I'm not a Dane, my work was more than appreciated all the time. Danish people are very supportive and encouraging. Since this period started, I became responsible for a store and for a team, therefore I gained experience in team-leading, and my time-management skill significantly improved." 
                :buttonData="{hasButton:false}"
                />

                <PositionComponent
                logo="netto-logo.png"
                title="NETTO - Sales Assistant"
                subTitle="2020 March - 2020 July"
                description = "In the beginning of the COVID-19 outbreak and quarantine-period I really wanted to try to find a way to help people, who are risked or affected by the virus-situation. As a student I didn't have too much possibilities, but I decided to apply to Netto, so I can help people day by day. At Netto, I met a wonderful team, and I got a taste from the Danish culture.
During my work in Netto as a Sales Assistant I gained really important practical skills regarding my future."
                :buttonData="{hasButton:false}"
                />
                
            </div >
            <div class ="flex-vertical">
                <TitleComponent title='EDUCATION'/>

                <PositionComponent
                logo="zealand.png"
                title="Zealand Academy - Computer Sciecne"
                subTitle="2019 - Present"
                description = "I am taking my current education in Denmark at Zealand Academy. I got hands on experience in programming and learned how project work really is. We have been tasked to deliver a solutions for real problems of a real companies. During my studies learned XAML, HTML, CSS, C#, SQL and Javascript as well. I got an overall understanding on the Agile software development process. During the project works we've been using XP and SCRUM."
                :buttonData="{icon: '&#xE890;', text: 'See grades', link: '', hasButton:true}"
                />

                <PositionComponent
                logo="tekologo.png"
                title="II. Rákóczi Ferenc Catholic Gymnasium - Kiskunhalas"
                subTitle="2015 - 2019"
                description = "I attended to the IT class of the school, where we got a basic understanding on how the computer is built. We learned about databases, used Microsoft Access and also mySQL. We have been tought networking, we got practical experience with CISCO devices (switches, routers etc..) During my secondary education I participated numerous competitions in programming, maths and physics. In my freetime I have been tutoring Maths and Physics."
                :buttonData="{icon: '&#xE890;', text: 'See diploma', link: '', hasButton:true}"
                />
            </div >
    </div>
    </div>

             <div id="extra-container">
                <div class="flex-container">
                    <div class ="flex-vertical">
                                <TitleComponent title='AWARDS'/>

                    </div >
                <div class ="flex-vertical">
                </div >
                </div>
             </div>
      </template>
    
  </div>
</template>


<script>
import ProfileComponent from './ProfileComponent'
import BlockInfoComponent from './BlockInfoComponent'
import TitleComponent from './TitleComponent'
import PositionComponent from './PositionComponent'

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
      ProfileComponent,
      TitleComponent,
      PositionComponent
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
       .flex-vertical
    {
        display: flex;
        flex-direction: column;
        width: 48%;
        margin: 0px auto;
        padding-bottom: 5%;
   }
   .background-container{
       background-image: url("../assets/bg-small7.gif"); 
       background-repeat:no-repeat;
       background-size: cover;
       padding-top: 5%;
       padding-bottom: 5%;
   }
   .extra-container
   {
       margin-top:4%;
   }
   

</style>
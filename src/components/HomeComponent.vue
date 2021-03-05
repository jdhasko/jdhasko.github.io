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
                        :buttonData="{icon: 'fas fa-cloud-download-alt fa-lg', text: 'download resume   ', link: 'https://github.com/jdhasko/jdhasko.github.io/tree/master/documents/cv.pdf', hasButton:true}" />

                        <BlockInfoComponent 
                        Title="EXPERIENCE" 
                        MarginSize='7'
                        :ListItemData="[
                        {topic: 'PROGRAMMING LANGUAGES', data:['Javascript, Typescript','HTML, CSS','C#','SQL', 'React', 'Vue'], oneline:0},
                        {topic: 'METHODOLOGIES', data:['Agile Developent', 'XP and SCRUM'], oneline:0},
                        {topic: 'OTHER', data:['UI Design - Prototyping','Adobe Ps, Pr, Xd etc.', 'Computer Networks'], oneline:0}]"
                        :buttonData="{icon: 'far fa-eye fa-lg', text: 'view grades ', link: 'https://github.com/jdhasko/jdhasko.github.io/tree/master/documents/grades.pdf', hasButton:true}" />
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
                description = "I am taking my current education in Denmark at Zealand Academy. I got hands-on experience in programming and learned how project work really is. We have been tasked to deliver solutions for real problems of real companies. I specialised in IT-Security, Mobile App Development (Android studio/Java/Kotling/Xamarin) and Unity Game Development. I also got a great understanding on how APIs structured and work.  "
                :buttonData="{icon: 'far fa-eye fa-lg', text: 'See grades', link: '', hasButton:true}"
                />

                <PositionComponent
                logo="tekologo.png"
                title="II. Rákóczi Ferenc Catholic Gymnasium - Kiskunhalas"
                subTitle="2015 - 2019"
                description = "I attended to the IT class of the school, where we got a basic understanding on how the computer is built. We learned about databases, used Microsoft Access and also mySQL. We have been tought networking, we got practical experience with CISCO devices (switches, routers etc..) During my secondary education I participated numerous competitions in programming, maths and physics. In my freetime I have been tutoring Maths and Physics."
                :buttonData="{ hasButton:false}"
                />
            </div >
    </div>
    </div>

             <div id="extra-background" class="extra-container">
                <div class="flex-container">
                    <div class ="flex-vertical">
                                <TitleComponent title='AWARDS'/>
                                <SmallBlockComponent
                                 title="STUDENT OF THE YEAR 2019"
                                 subTitle="II. Rákóczi Ferenc Catholic Gymnasium" 
                                :buttonData="{icon: 'far fa-eye fa-lg', text: 'See award', link: 'https://github.com/jdhasko/jdhasko.github.io/tree/master/documents/Student-of-the-year-award.pdf', hasButton:true}"/>

                                <SmallBlockComponent
                                 title="GRADUATION CERTIFICATE"
                                 subTitle="Praise for outstanding performance" 
                                :buttonData="{icon: '&#xE890;', text: 'See diploma', link: '', hasButton:false}"/>

                                 <SmallBlockComponent
                                 title="RECOMMENDATION"
                                 subTitle="from Csaba Péli Computer Engineer" 
                                :buttonData="{icon: 'far fa-eye fa-lg', text: 'Read document', link: 'https://github.com/jdhasko/jdhasko.github.io/tree/master/documents/Letter-of-Recommendation.pdf', hasButton:true}"/>
                    </div >
                <div class ="flex-vertical">
                      <TitleComponent title='VOLUNTARY WORKS'/>
                      <PositionComponent
                        logo=""
                        title="VOLUNTARY TUTOR IN MATHS AND PHYSICS"
                        subTitle="2017 - 2019"
                        description = "During my secondary education I have been taking Maths and Physics on the highest possible level. In my free time I have been tutoring a small group of students in both subjects. I was trying to prepare my fellow students to their exams with a different approach than what is usual in Hungary. I tried to bring the subject close to them with real life examples."
                        :buttonData="{ihasButton:false}"
                        />

                        <PositionComponent
                        logo=""
                        title="SERVICE AT THE LUTHERAN CHURCH"
                        subTitle="2014 - 2019"
                        description = "As a scout I have been actively supporting the local Lutheran Church and their nursing home. I participated in the organisation of many charity events during this time."
                        :buttonData="{ihasButton:false}"
                        />
                </div >
                </div>
             </div>
             <FooterComponent/>
      </template>
    
  </div>
</template>


<script>
import ProfileComponent from './ProfileComponent'
import BlockInfoComponent from './BlockInfoComponent'
import TitleComponent from './TitleComponent'
import PositionComponent from './PositionComponent'
import SmallBlockComponent from './SmallBlockComponent'
import FooterComponent from './FooterComponent'

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
      PositionComponent,
      SmallBlockComponent,
      FooterComponent
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
   #extra-background
   {
       background-image: url("../assets/bg6.gif");
       background-repeat: no-repeat;
       background-size: cover;
       padding: 4% 0px;
   }

   /**   MOBILE VIEW */
   
   @media only screen and (max-width:820px)
   {
    .flex-container
    {
        flex-direction: column;
        width: 90%;
    }
    .flex-vertical
    {
        width: 90%;
    }
    .caption 
    {
        top: 35%;
        width: 100%;
        text-align: center;
        color: white;
        font-size: 17px;
        line-break: strict;
        letter-spacing: 5px;
        white-space: nowrap;

    }

   }

</style>
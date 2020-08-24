<template>
<div>
  <div id="heroImage" class="sectionalPadding">
    <b-container>
      <b-row >
        <b-col>
          <b-row>
            <b-col class="text-center">
              <h1>Seconds Web Development</h1>
              <p>Hi, my name's Austin and I'm a Full Stack Web Developer in Davis/Weber county Utah.</p>
            </b-col>
          </b-row>
          <b-row>
            <b-col class="text-center">
              <b-button variant="success">Contact Me</b-button>
            </b-col>
          </b-row>
        </b-col>
      </b-row>
    </b-container>
  </div>
  <div class="topPadding">
    <b-container id="whyHire">
      <b-row class="pb-3"> 
        <b-col class="text-center">
          <h1>Why Work With Me?</h1>
        </b-col>
      </b-row>
      <b-row>
        <b-col sm="12" md="12" lg="4" xl="4" class="mx-auto pb-3" v-for="detail in details" :key="detail.title">
          <b-card
            :header="detail.title"
            header-class="text-center"
          >
            <b-card-text>{{ detail.description }}</b-card-text>
          </b-card>
        </b-col>
      </b-row> 
    </b-container>
  </div> 
  <div class="topPadding">
    <b-container fluid id="skills" class="topPadding">
      <b-row>
        <b-col cols="12" class="text-center">
          <h1>Skills</h1>
        </b-col>
      </b-row>
      <b-row class="mx-auto text-center pt-3">
        <b-col>
          <h3>Front End</h3>
          <b-row class="pt-3">
            <b-col sm="6" md="6" lg="3" xl="3" v-for="skill in frontEndSkills" :key="skill.title" style="padding-bottom: 15px">
              <Skill :title="skill.title" :img="skill.img" />
            </b-col>
          </b-row>
        </b-col>
      </b-row>
      <b-row class="mx-auto text-center pt-3">
        <b-col>
          <h3>Back End</h3>
          <b-row class="pt-3"> 
            <b-col sm="6" md="6" lg="3" xl="3" v-for="skill in backEndSkills" :key="skill.title" style="padding-bottom: 15px">
              <Skill :title="skill.title" :img="skill.img" />
            </b-col>
          </b-row>
        </b-col>
      </b-row>
      <b-row class="mx-auto text-center pt-3">
        <b-col>
          <h3>Database</h3>
          <b-row class="pt-3">
            <b-col sm="6" md="6" lg="3" xl="3" v-for="skill in databaseSkills" :key="skill.title" style="padding-bottom: 15px">
              <Skill :title="skill.title" :img="skill.img" />
            </b-col>
          </b-row>
        </b-col>
      </b-row>
      <b-row class="mx-auto text-center pt-3">
        <b-col>
          <h3>Frameworks</h3>
          <b-row class="pt-3">
            <b-col sm="6" md="6" lg="3" xl="3" v-for="skill in frameworks" :key="skill.title" style="padding-bottom: 15px">
              <Skill :title="skill.title" :img="skill.img" />
            </b-col>
          </b-row>
        </b-col>
      </b-row>
    </b-container>
  </div>
</div>
</template>

<script>
import Skill from '../components/skill'

export default {
  components: {
    Skill
  },
  data: () => {
    return {
      frontEndSkills: [
        {
          title: 'Vue Js',
          img: 'vuejs.png',
        },
        {
          title: 'HTML',
          img: 'html5logo.png'
        },
        {
          title: 'CSS',
          img: 'cssLogo.png'
        },
        {
          title: 'Javascript',
          img: 'JSLogo.png'
        }
      ],
      backEndSkills: [
        {
          title: 'C#',
          img: 'csharpLogo.png'
        },
        {
          title: 'Node.js',
          img: 'nodeJsLogo.png'
        },
      ],
      databaseSkills: [
        {
          title: 'SQL Server',
          img: 'SqlServer.svg'
        },
        {
          title: 'Postgres',
          img: 'Postgresql.png'
        },
        {
          title: 'Mongo DB',
          img: 'mongodb.png'
        }
      ],
      frameworks: [
        {
          title: 'Ember JS',
          img: 'emberjs.png'
        },
        {
          title: 'ASP.Net',
          img: 'aspdotnet.png'
        }
      ],
      details: [
        {
          title: 'Experience',
          description: "I have been a Full Stack Web Developer since 2018, and during that time I've built multiple websites, desktop applications, and mobile apps. You can view some of my work here: ADD PAGE LINK"
        },
        {
          title: 'Innovative',
          description: "You want to do something new and clever? Let me know! I'm always up for a challenge whether that be in building a complicated interface, or using a technology I don't know."
        },
        {
          title: 'Customer Satisfaction',
          description: "My goal is to build an application that meets all of your expectations. If there's something that you want changed or added to your application, let me know and I'll make it happen."
        }
      ]
    }
  }
}
</script>

<style>
#heroImage {
  background-image: url('../assets/heroBackground.png');
  background-size: cover;
}

#whyChooseMe {

}

.sectionalPadding {
  padding-top: 5rem;
  padding-bottom: 5rem;
}

.topPadding {
  padding-top: 5rem;
}

#skills {
  background-color: #c9e1ff;
}

#csharpSkill {
  background-color: lightgrey;
}

#javascriptSkill {
  background-color: lightgrey;
}
</style>
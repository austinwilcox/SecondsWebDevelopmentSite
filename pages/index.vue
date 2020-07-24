<template>
  <div>
    <div id="heroImage" class="section">
      <b-container>
        <h1 class="text-center text-white" style="padding-top: 350px;">
          Seconds <br /> Web Development
        </h1>
        <p class="text-center text-white">Hi, my name's Austin and I'm a Freelance Full Stack Web Developer in Davis/Weber County Utah.</p>
        <b-row>
          <b-col class="text-center">
            <b-button variant="danger" id="contactMeButton" class="text-white" href="mailto: austin21wilcox@gmail.com">Contact Me</b-button>
          </b-col>
        </b-row>
      </b-container>
    </div>
    <div id="education" class="section">
      <b-container>
        <h1 class="text-center">
          Education
        </h1>
        <b-row>
          <b-col sm="12" md="12" lg="12" xl="12">
            <b-card
              title="Computer Science - Bachelors Degree"
              img-src="../assets/weberStateWildcat.png"
              img-alt="Weber State Wildcat"
              img-width="175"
              img-height="127.148437"
              img-left
              class="m-2"
            >
              <b-card-subtitle class="small text-muted">Fall 2015 - Fall 2019</b-card-subtitle>
              <b-card-text>
                Weber State University, Ogden, Utah
              </b-card-text>
            </b-card>
          </b-col>
        </b-row>
      </b-container>
    </div>
    <div id="jobs" class="section">
      <b-container>
        <h1 class="text-center text-white" style="padding-bottom: 15px;">
          Job Experience
        </h1>
        <b-row>
          <b-col v-for="job in jobs" :key="job.title" sm="12" md="12" lg="6" xl="6">
            <b-card
              class="mb-2"
            >
            <b-img :src="job.img" :alt="job.company" :width="job.imgWidth" :height="job.imgHeight"></b-img>
            <b-card-title :title="job.title"></b-card-title>
              <b-card-text>
                {{job.company}}
              </b-card-text>
              <b-card-subtitle class="small text-muted">
                {{job.hireDate}} - {{job.endDate}}
              </b-card-subtitle>
              <b-card-text>
                {{job.description}}
              </b-card-text>
              <div style="paddingTop: 20px; paddingBottom: 20px;">
                <b-button :class="job.detailsVisible ? null : 'collapsed'" :aria-expanded="job.detailsVisible ? 'true' : 'false'" @click="job.detailsVisible = !job.detailsVisible" variant="primary">Details</b-button>
                <b-collapse :id="job.id" v-model="job.detailsVisible" class="mt-2">
                  <b-table striped hover :items="job.accomplishments" fields="[]">
                  </b-table>
                </b-collapse>
              </div>
              <b-badge pill variant="light" v-for="tool in job.tools" :key="tool" style="margin: 5px; padding: 10px;">{{tool}}</b-badge>
            </b-card>
          </b-col>
        </b-row>
      </b-container>
    </div>
    <div id="skills">
      <b-container>
        <h1 class="text-center section">
          Skills
        </h1>
        <b-row>
          <b-col sm="12" md="6" lg="4" xl="3" v-for="skill in skills" :key="skill.name">
            <div class="text-center" style="paddingTop: 20px;">
              <b-img :src="skill.img" fluid :alt="skill.name" width="75" height="75"></b-img>
              <h4 style="paddingTop: 25px;">{{skill.name}}</h4>
            </div>
          </b-col>
        </b-row>
      </b-container>
    </div>
  </div>
</template>

<script>
export default {
  head() {
    title: 'Seconds Web Dev'
  },
  data: () => {
    return {
      skills: [
        {
          category: 'Desktop',
          name: 'Electron',
          img: require("../assets/ElectronLogo.png"),
          details: ""
        },
        {
          category: 'Desktop',
          name: 'Windows Forms',
          img: require("../assets/VisualStudio2017Logo.png"),
          details: ''
        },
        {
          category: 'Front End',
          name: 'Vue Js',
          img: require("../assets/VueLogo.png"),
          details: ''
        },
        {
          category: 'Back End',
          name: 'Node Js',
          img: require("../assets/nodeJsLogo.png"),
          details: ''
        },
        {
          category: 'Back End',
          name: 'C#',
          img: require("../assets/csharpLogo.png"),
          details: ''
        },
        {
          category: 'Framework',
          name: 'Web Forms',
          img: require("../assets/aspnet.png"),
          details: ''
        },
        {
          category: 'Database',
          name: 'Postgresql',
          img: require("../assets/Postgresql.png"),
          details: ''
        },
        {
          category: 'Database',
          name: 'Sql Server',
          img: require("../assets/SqlServer.svg"),
          details: ''
        },
        {
          category: 'Mobile',
          name: 'Swift',
          img: require("../assets/swiftLogo.png"),
          details: ''
        },
        {
          category: 'Server',
          name: 'Ubuntu',
          img: require("../assets/ubuntu.png"),
          details: ''
        }
      ],
      jobs: [
        {
          id: 1,
          title: 'Full Stack Developer',
          company: 'Weber Basin Water Conservancy District',
          img: require("../assets/districtlogo.png"),
          imgWidth: 456.488,
          imgHeight: 150,
          description: 'Programmer, developed web forms, windows forms, api services, and IOS mobile applications.',
          hireDate: 'November 2018',
          endDate: 'Current',
          detailsVisible: false,
          tools: [
            "Web Forms",
            "C#",
            "Windows Forms",
            "ASP.NET",
            "IIS",
            "Web Api",
            "Swift",
            "Sql Server"
          ],
          accomplishments: [
            {
              label: 'Inventory',
              details: 'Designed and built an inventory system to manage the several warehouses.'
            },
            {
              label: 'Subdivision Management System',
              details: 'TODO'
            }
          ]
        },
        {
          id: 2,
          title: 'Lead Developer',
          company: 'The League Esports',
          img: require("../assets/tleLogo.png"),
          imgWidth: 150,
          imgHeight: 150,
          description: 'Lead developer/architect in developing the site and applications.',
          hireDate: 'January 2020',
          endDate: 'Current',
          detailsVisible: false,
          tools: [
            "Vue",
            "Nuxt",
            "Node",
            "Postgres",
            "Ubuntu",
            "Nginx",
            "SEO"
          ],
          accomplishments: [
            {
              label: 'Site',
              details: 'Designed and built the entire site/application from scratch'
            }
          ]
        }
      ]
    }
  }
}
</script>

<style>
body {
  font-family: Arial, Helvetica, sans-serif;
  font-size: 20px;
}

.section {
  padding-top: 20px;
  padding-bottom: 20px;
}

#heroImage {
  background-image: url('../assets/smokeBackground.png');
  background-color: aliceblue;
  background-size: cover;
  height: 1000px;
}

#contactMeButton {
  padding: 10px;
}

#education {
  padding-bottom: 70px;
}

#jobs {
  background-color: grey;
}
</style>

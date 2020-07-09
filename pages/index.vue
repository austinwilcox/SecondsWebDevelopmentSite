<template>
  <div>
    <h1 class="text-center">
      Seconds <br /> Web Development
    </h1>
    <p class="text-center">Hi, my name's Austin and I'm a Freelance Full Stack Web Developer in Davis/Weber County Utah.</p>
    <b-button variant="outline-success">Contact Me</b-button>
    <h1 class="text-center">
      Job Experience
    </h1>
    <b-row>
      <b-col v-for="job in jobs" :key="job.title" sm="12" md="12" lg="6" xl="6">
        <b-card
          :title="job.title"
          :img-src="job.img"
          :img-alt="job.company"
          img-top
          class="mb-2"
        >
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
    <div id="skills">
      <h1 class="text-center">Skills</h1>
      <b-row>
        <b-col sm="12" md="6" lg="4" xl="3" v-for="skill in skills" :key="skill.name">
          <div class="text-center" style="paddingTop: 20px;">
            <b-img :src="skill.img" fluid :alt="skill.name" width="75" height="75"></b-img>
            <h4 style="paddingTop: 25px;">{{skill.name}}</h4>
          </div>
        </b-col>
      </b-row>
    </div>
  </div>
</template>

<script>
export default {
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
          img: require("../assets/csharplogo.png"),
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
        }
      ],
      jobs: [
        {
          id: 1,
          title: 'Programmer',
          company: 'Weber Basin Water Conservancy District',
          img: require("../assets/districtlogo.png"),
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
          img: "http://theleagueesports.com/media/tle-logo.png",
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
</style>

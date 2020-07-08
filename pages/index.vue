<template>
  <div>
    <h1 class="text-center">
      Seconds <br /> Web Development
    </h1>
    <p class="text-center">Hi, my name's Austin and I'm a Freelance Full Stack Web Developer in the Davis/Weber County Utah area.</p>
    <b-button variant="outline-success">Contact Me</b-button>
    <h1 class="text-center">
      Job Experience
    </h1>
    <b-row>
      <b-col v-for="job in jobs" :key="job.title" sm="12" md="12" lg="12" xl="12">
        <h1>{{job.title}}</h1>
      </b-col>
    </b-row>
  </div>
</template>

<script>
export default {
  data: () => {
    return {
      jobs: [
        {
          title: 'Programmer',
          description: 'Programming all kinds of things',
          hireDate: '',
          endDate: '',
          accomplishments: [
            {
              label: '',
              details: ''
            },
            {
              label: '',
              details: ''
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

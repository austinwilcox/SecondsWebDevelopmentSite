<template>
  <b-card bg-variant="secondary" class="text-center">
    <b-button v-for="icon in icons" :key="icon.icon" :href="icon.to" variant="primary" class="px-3 mx-2 my-2" target="blank">{{icon.icon}}</b-button>
    <strong><hr /></strong>
    <b-card-text class="text-center">
      2020 - Seconds Web Development
    </b-card-text>
  </b-card>
</template>

<script>
export default {
  data: () => {
    return {
      icons: [
        {
          icon: 'email',
          to: 'mailto: austin21wilcox@gmail.com'
        },
        {
          icon: 'github',
          to: 'https://github.com/austinwilcox'
        },
        {
          icon: 'linkedin',
          to: 'https://www.linkedin.com/in/austin-wilcox-3193a4106/'
        },
        {
          icon: 'twitter',
          to: 'https://twitter.com/Seconds21ive'
        }
      ]
    }
  }
}
</script>

<style>

</style>
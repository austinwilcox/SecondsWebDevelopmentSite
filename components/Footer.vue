<template>
  <b-card bg-variant="primary">
    <b-button v-for="icon in icons" :key="icon.icon" :href="icon.to" target="blank">{{ icon.icon }}</b-button>
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
          icon: 'Email',
          to: '/contactme'
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
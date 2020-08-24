<template>
  <div>
    <h5>{{title}}</h5>
    <b-img :src="require(`../assets/${img}`)" width="100" height="100" :alt="title"></b-img>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
    img: String
  }
}
</script>

<style>

</style>
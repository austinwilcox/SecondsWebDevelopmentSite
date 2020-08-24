<template>
  <div>
   <b-container>
      <b-row>
        <b-col v-if="codeSnippets.length > 0">

        </b-col>
        <b-col v-else>
          <h1>No Code Snippets Saved Yet</h1>
        </b-col>
      </b-row>  
   </b-container> 
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: 'Code Snippets'
    }
  },
  data: () => {
    return {
      codeSnippets: []
    }
  }
}
</script>

<style>
</style>
<template>
<div>
  <h1>About Page</h1>
  <h2>{{ subtitle }}</h2>
</div>
</template>

<script>
  export default {
    data(){
      return {
        subtitle: 'この文書'
      }
    },

    head(){
      return {
        title: 'About Page'
      }
    }
  }
</script>

<template>
<div>
  <h1>About Page</h1>
  <h2>{{ subtitle }}</h2>
  <v-breadcrumbs :items="items"></v-breadcrumbs>
</div>
</template>

<script>
  export default {
    data(){
      return {
        subtitle: 'この文書',
        items: [
          {
            text: "root",
            disabled: false,
            href: 'vuetify_v-breadcrumbs.html',
          },
          {
            text: "subdir1",
            disabled: false,
            href: 'vuetify_v-breadcrumbs1.html',
          },
          {
            text: "subdir2",
            disabled: true,
            href: 'vuetify_v-breadcrumbs2.html',
          },
        ]
      }
    },

    head(){
      return {
        title: 'About Page'
      }
    }
  }
</script>

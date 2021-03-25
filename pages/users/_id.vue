<template>
    <h1>ユーザID: {{ user.name }}</h1>
</template>

<script>
export default ({
  head(){
    return {
      title: this.user.name,
      meta:[
        { hid: 'description', name: 'description', content: 'これはAboutページです。'}
      ]
    }
  },
  data(){
    return {
      id: this.$route.params.id,
      users: [
        {
          id: 1, name: 'John Doe'
        },
        {
          id: 2, name: 'Kevin Smith'
        },
        {
          id: 3, name: 'Harry Bosch'
        },
      ],
    }
  },
  computed: {
    user(){
      return this.users.find(user => user.id == this.id)
    }
  }
})
</script>

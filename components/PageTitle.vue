<template>
  <div>
    <nav>
    <nuxt-link to="/">Home</nuxt-link>
    <nuxt-link :to="{ name: 'about' }" no-prefetch>About</nuxt-link>
    <nuxt-link :to="{ name: 'about' }">About</nuxt-link>
    <nuxt-link :to="{ name: 'users-list' }">User List</nuxt-link>
    </nav>
  </div>
</template>
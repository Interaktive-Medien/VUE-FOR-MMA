<template>
  <nav>
    <router-link to="/">Home Home</router-link> |
    <router-link to="/about">About</router-link>
  </nav>
  <router-view/>
</template>

<style>

body {
  padding: 50px;
}

nav {
  margin-bottom: 50px;
}

</style>

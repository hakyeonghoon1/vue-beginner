<template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link> |
    <router-link to="/databinding/string">String</router-link> |
    <router-link to="/databinding/html">HTML</router-link> |
    <router-link to="/databinding/input">Input</router-link> |
    <router-link to="/databinding/select">Select</router-link> |
    <router-link to="/databinding/Checkbox">Checkbox</router-link> |
    <router-link to="/databinding/Radio">Radio</router-link> |
    <router-link to="/databinding/Attr">Attr</router-link> |
    <router-link to="/databinding/List">List</router-link> |
    <router-link to="/databinding/Class">Class</router-link> |
    <router-link to="/databinding/Style">Style</router-link> |
    <router-link to="/databinding/click">Click</router-link> |
    <router-link to="/databinding/change">Change</router-link> |
    <router-link to="/databinding/key">Key</router-link> |
  </nav>
  <router-view />
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>

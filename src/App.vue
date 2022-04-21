<template>
  <div id="app">
    <h1>Todo App</h1>
    <hr>

    <router-view />
    <router-link to="/">Home</router-link>
  </div>
</template>


<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

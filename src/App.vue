<template>
  <div id="app">
   <NavBar />
   <MainContent />
   <PageFooter />
  </div>
</template>

<script>

import NavBar from "./components/NavBar.vue"
import MainContent from "./components/MainContent.vue"
import PageFooter from "./components/PageFooter.vue"

export default {
  name: 'App',
  components: {
    NavBar,
    MainContent,
    PageFooter
  }
}
</script>

<style lang="scss">
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  ul{
    list-style: none;
  }
#app {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
</style>

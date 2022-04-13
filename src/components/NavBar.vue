<template>
  <div id="navbar">
    <div>
      <img :src="`${publicPath}img/dc-logo.png`" alt="logo" />
    </div>
    <div>
      <NavBarList />
    </div>
  </div>
</template>

<script>

import NavBarList from "./NavBarList.vue"

export default {
  data(){
    return{
      publicPath: process.env.BASE_URL,
    }
  },
  name: "NavBar",
  components: {
    NavBarList
  }
  
};
</script>

<style scoped lang="scss">
#navbar{
  padding: 10px 15% 0;
  display: flex;
  justify-content: space-between;
}
</style>

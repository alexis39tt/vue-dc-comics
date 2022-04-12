<template>
  <div id="navbar">
    <div>
      <img src="../assets/img/dc-logo.png" alt="logo" />
    </div>
    <div>
      <NavBarList />
    </div>
  </div>
</template>

<script>

import NavBarList from "./NavBarList.vue"

export default {
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

<template>
  <div id="maincontent">
    <div class="text">
      <h1>Content goes here</h1>
    </div>
    <div class="mainbar">
        <MainBar />
    </div>
  </div>
</template>

<script>
import MainBar from "./MainBar.vue";

export default {
  name: "MainContent",
  components:{
      MainBar
  }
};
</script>

<style lang="scss">
#maincontent{
    color: white;
    background: black;
    h1{
        padding: 50px 15%;
    }
}

</style>
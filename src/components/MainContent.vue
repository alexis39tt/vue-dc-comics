<template>
  <div id="maincontent">
    <div id="banner">
      <img src="../../public/img/jumbotron.jpg" alt="banner" />
    </div>
    <div id="title">
      <p>CURRENT SERIES</p>
    </div>
    <div id="cards">
      <CardComp v-for="(elm, i) in cards" :key="i" :card="elm" />
    </div>
    <div>
      <button>LOAD MORE</button>
    </div>
    <div>
      <MainBar />
    </div>
  </div>
</template>

<script>
import cards from "../../public/jsons/dc-comics.json";
import CardComp from "./CardComp.vue";
import MainBar from "./MainBar.vue";

export default {
  name: "MainContent",
  components: {
    CardComp,
    MainBar,
  },
  data() {
    return {
      cards: cards,
    };
  },
};
</script>

<style lang="scss">
#maincontent {
  color: white;
  background: #1c1c1c;
  #banner {
    max-height: 400px;
    overflow: hidden;
    img {
      width: 100%;
    }
  }
  #title {
    margin: -18px 15% 30px;
    p {
      font-weight: bold;
      background: #0a82f9;
      font-size: 24px;
      display: inline;
      padding: 10px 25px;
    }
  }
  #cards{
    display: flex;
    flex-wrap: wrap;
    margin: 0 15%;
    }
    button{
      display: flex;
      color: white;
      font-weight: 800;
      background: #0a82f9;
      padding: 10px 75px;
      margin: -30px auto 20px;
      border: none;
      cursor: pointer;
      &:hover{
        background: #2592ff;
      }
    }
}
</style>
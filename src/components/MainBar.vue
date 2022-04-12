<template>
  <div id="mainbar">
    <div v-for="(elm, i) in mainbarlist" :key="i" class="list-item">
      <img :src="`${publicPath}img/buy-${elm.imgurl}`" :alt="`${elm.name}`">
      <p>{{ elm.name }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "MainBar",
  data() {
    return {
      publicPath: process.env.BASE_URL,
      mainbarlist: [
        {
          name: "Digital Comics",
          imgurl: "comics-digital-comics.png",
        },
        {
          name: "DC Merchandise",
          imgurl: "comics-merchandise.png",
        },
        {
          name: "Subscription",
          imgurl: "comics-subscriptions.png",
        },
        {
          name: "Comic shop locator",
          imgurl: "comics-shop-locator.png",
        },
        {
          name: "DC Power visa",
          imgurl: "dc-power-visa.svg",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
#mainbar {
  background: #0282f9;
  display: flex;
  justify-content: center;
  padding: 50px 0;
  p {
    text-transform: uppercase;
  }
  .list-item{
      display: flex;
      margin: 0 10px;
      img{
          min-width: 10%;
      }
  }
}
</style>

<template>
  <div id="mainbar">
    <div v-for="(elm, i) in mainbarlist" :key="i" class="list-item">
      <img :src="`${publicPath}img/buy-${elm.imgurl}`" :alt="`${elm.name}`" />
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
  padding: 20px 0;
  .list-item {
    display: flex;
    cursor: pointer;
    z-index: 2;
    &:hover {
      img {
          transform: scale(1.1);
      }
      p{
          text-decoration: underline;
      }
    }
    img {
      max-width: 40%;
      height: 60%;
      margin: auto 20px;
      transition: 0.2s;
    }
    p {
      text-transform: uppercase;
      margin: auto 0;
      min-width: 120px;
    }
  }
}
</style>

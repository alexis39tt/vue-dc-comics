<template>
  <div id="footer">
    <div id="topbar">
        <div id="cols">
            <div>
                <h2>DC COMICS</h2>
                <ul>
                <li v-for="(elm, i) in dc_comics" :key="i">{{ elm }}</li>
                </ul>
                <h2>SHOP</h2>
                <ul>
                <li v-for="(elm, i) in shop" :key="i">{{ elm }}</li>
                </ul>
            </div>
            <div>
                <h2>DC</h2>
                <ul>
                <li v-for="(elm, i) in dc" :key="i">{{ elm }}</li>
                </ul>
            </div>
            <div>
                <h2>SITES</h2>
                <ul>
                <li v-for="(elm, i) in sites" :key="i">{{ elm }}</li>
                </ul>
            </div>
        </div>
        <div>
            <img :src="`${publicPath}img/dc-logo-bg.png`" alt="logo">
        </div>
    </div>
    <BottomBar />
  </div>
</template>

<script>
import BottomBar from "./BottomBar.vue";

export default {
  name: "PageFooter",
  components: {
    BottomBar,
  },
  data() {
    return {
        publicPath: process.env.BASE_URL,
        dc_comics: ['Characters', 'Comics', 'Movies', 'TV', 'Games', 'Videos', 'News'],
        shop: ['Shop DC', 'Shop DC Collectibles'],
        dc: ['Terms Of Use', 'Privacy policy (New)', 'Ad Choices', 'Advertising', 'Jobs', 'Subscriptions', 'Talent Workshops', 'CPSC Certificates', 'Ratings', 'Shop Help', 'Contact Us'],
        sites: ['DC', 'MAD Magazine', 'DC Kids', 'DC Universe', 'DC Power Visa']
    };
  },
};
</script>

<style scoped lang="scss">
#footer {
  #topbar{
      display: flex;
      justify-content: space-between;
      padding: 0 15%;
      background-image: url("../../public/img/footer-bg.jpg");
      background-repeat: no-repeat;
      background-size: cover;
      #cols{
          display: flex;
          margin: 30px 0;
          div{
              margin-right: 30px;
          }
          h2{
              color: white;
              margin: 10px 0;
          }
          li{
              color: gray;
              cursor: pointer;
              &:hover{
                  color: white;
              }
          }
      }
      img{
          margin: -95px 0;
          overflow-y: hidden;
          z-index: 1;
      }
  }
}

</style>
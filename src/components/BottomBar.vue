<template>
  <div id="bottombar">
    <div>
      <button>SIGN-UP NOW!</button>
    </div>
    <div id="socials">
      <h2>FOLLOW US</h2>
      <div id="imgcontainer">
        <div v-for="(elm, i) in socials" :key="i">
          <img
            :src="`${publicPath}img/footer-${elm.imgurl}.png`"
            :alt="`${elm.name}`"
          />
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "BottomBar",
  data() {
    return {
      publicPath: process.env.BASE_URL,
      socials: [
        {
          name: "facebook",
          imgurl: "facebook",
        },
        {
          name: "twitter",
          imgurl: "twitter",
        },
        {
          name: "youtube",
          imgurl: "youtube",
        },
        {
          name: "pinterest",
          imgurl: "pinterest",
        },
        {
          name: "periscope",
          imgurl: "periscope",
        },
      ],
    };
  },
};
</script>
<style scoped lang="scss">
$dcblue: #0282f9;
#bottombar {
  background: #303030;
  display: flex;
  justify-content: space-between;
  padding: 30px 15%;
  button {
    border: 2px solid $dcblue;
    color: white;
    padding: 15px;
    background: none;
    font-size: 1rem;
    font-weight: bold;
    cursor: pointer;
    transition: 0.2s;
    &:hover {
      color: $dcblue;
      background: white;
    }
  }
  #socials{
      display: flex;
      line-height: 52px;
      h2{
          color: $dcblue;
          margin-right: 20px;
      }
      #imgcontainer{
          display: flex;
          img{
              padding: 0 10px;
              vertical-align: -12px;
              cursor: pointer;
              transition: 0.2s;
              &:hover{
                  filter:brightness(1.2)
              }
          }
      }
  }
}
</style>
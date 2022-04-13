<template>
    <ul>
      <li v-for="(elm, i) in navbarlist" :key='i' :class="elm.selected && 'selected'">
        <a :href="`${elm.url}`">{{elm.name}}</a>
      </li>
    </ul>
</template>

<script>
export default {
data() {
    return{
      navbarlist: [
        {
          name: 'Characters',
          url: '/characters',
          selected: false
        },
        {
          name: 'Comics',
          url: '/comics',
          selected: true
        },
        {
          name: 'Movies',
          url: '/movies',
          selected: false
        },
        {
          name: 'TV',
          url: '/tv',
          selected: false
        },
        {
          name: 'Games',
          url: '/games',
          selected: false
        },
        {
          name: 'Collectibles',
          url: '/collectibles',
          selected: false
        },
        {
          name: 'Videos',
          url: '/videos',
          selected: false
        },
        {
          name: 'Fans',
          url: '/fans',
          selected: false
        },
        {
          name: 'News',
          url: '/news',
          selected: false
        },
        {
          name: 'Shop',
          url: '/shop',
          selected: false
        },
      ]
    }
  }
}
</script>
<style scoped lang="scss">
$dcblue: #0282f9;
ul{
    display: flex;
    text-transform: uppercase;
    font-weight: bold;
    margin: 0;
    a{
        text-decoration: none;
        color: rgb(48, 48, 48);
        transition: 0.2s;
    }
    li{
        margin: 0 10px;
        line-height: 105px;
        transition: 0.2s;
        &:hover{
          border-bottom: 5px solid $dcblue;
          a{
            color: $dcblue;
          }
        }
    }
    li.selected{
        border-bottom: 5px solid $dcblue;
        a{
          color: $dcblue
        }
    }
}
</style>
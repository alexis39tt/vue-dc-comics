<template>
  <div class="card">
    <div class="cardimg">
      <img :src="card.thumb" :alt="card.series" />
    </div>
    <div class="cardtext">
      <p>{{ card.series }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardComp",
  props: {
    card: Object,
  },
};
</script>

<style lang="scss">
.card {
    margin: 0 15px 0;
    cursor: pointer;
    transition: 0.2s;
    &:hover{
        transform: scale(1.1);
        .cardtext{
            color: #0a82f9;
        }
    }
    .cardimg{
        width: 100%;
        height: 60%;
        overflow: hidden;
    }
    .cardtext {
        transition: 0.2s;
    p {
      text-transform: uppercase;
      max-width: 192px;
      margin-top: 15px;
      max-height: 50px;
    }
  }
}
</style>
<template>
    <div>
      <mt-swipe :auto="4000">
        <mt-swipe-item v-for="item in lunbotuList" :key="item.url">
          <img :src="item.img" alt="" :class="{ 'full': isfull }">
        </mt-swipe-item>
      </mt-swipe>
    </div>
</template>

<script>
    export default {
      name: "swiper",
      props: ['lunbotuList',"isfull"]
    }
</script>

<style lang="scss" scoped>
  .mint-swipe {
    height: 200px;

    .mint-swipe-item {
      &:nth-child(1) {
      background-color: greenyellow;
      }
      &:nth-child(2) {
      background-color: #f40;
      }
      &:nth-child(3) {
      background-color: cyan;
      }

      img {
        width: 100%;
        height: 100%;
      }
    }
  }
  .full {
    width: 100%;
  }
</style>

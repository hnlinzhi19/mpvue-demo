<template>
  <div>
    <a v-if="isLink && href" class="lz-cell" :hover-class="(isLink && href) ? 'weui-cell_active' : 'none'" @click="$emit('click', $event)"
      :href="href">
      <img v-if="icon" :src="icon"> {{text}}
      <span class="icon-link"></span>
    </a>
    <div v-else class="lz-cell" :hover-class="(isLink && href) ? 'weui-cell_active' : 'none'">
      <img v-if="icon" :src="icon"> {{text}}
    </div>
  </div>

</template>

<script>
  export default {
    name: 'lix',
    props: {
      icon: {
        type: String,
      },
      text: {
        type: String,
      },
      isLink: {
        type: Boolean,
      },
      href: {
        type: String,
      },
    },
    data() {
      return {};
    },
    methods: {

    },
  };

</script>

<style lang="scss">
  .lz-cell {
    width: 100%;
    position: relative;
    padding-right: 60px;
    padding-left: 20px;
    box-sizing: border-box;
    border-bottom: 1rpx solid #ddd;
    line-height: 80px;
    transition: all 0.2s ease;
    &.weui-cell_active {
      background: #eee;
    }
    img {
      width: 60px;
      height: 60px;
      line-height: 80px;
      margin-top: 20px;
      position: relative;
      top: 15px;
    }
    .icon-link {
      position: absolute;
      right: 10px;
      top: 50%;
      display: block;
      width: 40px;
      height: 40px;
      background: url(../../static/images/right.png) no-repeat top center;
      background-size: 100%;
      transform: translate(0, -50%);
    }
  }

</style>

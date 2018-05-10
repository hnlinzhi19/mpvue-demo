<template>
  <div class="page-user">
    <div class="user-list">
      <card :text="motto"></card>
      <lz-cell :text="motto" :icon="home" href="/pages/logs/main" :isLink="true"></lz-cell>
      <lz-cell :text="motto" :isLink="true"></lz-cell>
    </div>
  </div>
</template>

<script>
import card from '@/components/card';
import lzCell from '@/components/lzCell';
import home from '../../../static/images/home.png';

export default {
  data() {
    return {
      motto: 'Hello World',
      userInfo: {},
      num: 1,
      home,
    };
  },
  components: {
    card,
    lzCell,
  },
};
</script>

<style  lang="scss">
.page-user{
  width: 100%;
  .user-list{
    width: 100%;
  }
}
</style>

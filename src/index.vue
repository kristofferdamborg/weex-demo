<template>
  <div class="wrapper" @click="update">
    <image :src="logoUrl" class="logo"></image>
    <text class="title">Hi {{target}}</text>
    <text class="desc">Now, let's use vue to build your weex app.</text>
    <list class="list">
      <cell class="cell" v-for="num in lists" :key="num">
        <div class="panel">
          <text class="text">{{ num }}</text>
        </div>
      </cell>
    </list>
  </div>
</template>

<style>
  .wrapper { align-items: center; margin-top: 120px; }
  .title { padding-top:40px; padding-bottom: 40px; font-size: 48px; }
  .logo { width: 360px; height: 156px; }
  .desc { padding-top: 20px; color:#888; font-size: 24px;}
</style>

<script>
  export default {
    data () {
      return {
        logoUrl: 'http://img1.vued.vanthink.cn/vued08aa73a9ab65dcbd360ec54659ada97c.png',
        target: 'World',
        lists: [ 'A', 'B', 'C', 'D', 'E']
      }
    },
    methods: {
      update: function (e) {
        this.target = 'Weex'
        console.log('target:', this.target)
      }
    }
  }
</script>
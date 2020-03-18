<template>
  <view>
    <div v-for="item in dataList" :key="item.did" style="padding-bottom: 5px">
      <i-card :title="item.name" :extra="item.systemNumber" @click="clickCard(item)">
        <view slot="content"  >{{item.systemStatus}}</view>
        <view slot="footer"   >{{item.sysniche}}</view>
      </i-card>
    </div>
  </view>
</template>

<script>
  export default {
    data () {
      return {
      }
    },
    props: [
      'dataList',
      'current'
    ],
    components: {
    },
    methods: {
      clickCard (item) {
        mpvue.navigateTo({url: '../pages/applicationSystem/systemForm/main'})
        // this.$router.push({
        //   path: '../pages/applicationSystem/systemForm/main'
        // })
      }
    }
  }
</script>

<style>
</style>

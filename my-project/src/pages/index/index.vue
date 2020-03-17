<template>
  <div>
    <i-button type="primary" @click="fillApplicationSystemInfo">填写应用系统信息</i-button>
    <i-button type="primary" @click="fillFunctionModuleInfo">填写功能模块信息</i-button>
  </div>
</template>


<script>
  export default {
    data () {
      return {
      }
    },

    components: {
    },

    methods: {
      fillApplicationSystemInfo () {
        this.$router.push({path: '/pages/applicationSystem/main'})
      },
      fillFunctionModuleInfo () {
        console.log('222222')
        // this.$router.push({path: '/pages/applicationSystem/main'})
      },
      created () {
        // let app = getApp()
      }
    }

  }
</script>

<style scoped>

</style>

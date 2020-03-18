<template>
  <div>
    <my-component-card v-bind:current="current" v-bind:dataList="draftList" ></my-component-card>
    <i-tab-bar :current="current" :fixed=true @change="handleChange">
      <i-tab-bar-item key="brush" icon="brush" current-icon="brush_fill" title="草稿"></i-tab-bar-item>
      <i-tab-bar-item key="task" icon="task" current-icon="task_fill" title="待审核"></i-tab-bar-item>
      <i-tab-bar-item key="undo" icon="undo" current-icon="undo" count="3" title="被驳回"></i-tab-bar-item>
      <i-tab-bar-item key="success" icon="success" current-icon="success_fill" title="审核通过"></i-tab-bar-item>
    </i-tab-bar>
  </div>
</template>

<script>
  import Card from '@/components/card.vue'
  export default {
    data () {
      return {
        current: 'brush',
        draftList: [
          {
            did: '1',
            name: '综合前置系统',
            systemNumber: '1101',
            systemStatus: '待上线',
            sysniche: '临柜前端系统，可实现密码器，读卡器等设备管理与配置，集成批量报表查询打印，指纹收集和校验，密钥下载更新，参数下载同步，远程授权等各种业务前端功能，同时接入大信贷，会计管理、理财销售、电子影像等多业务渠道，用以支持多样稳定，风险可控的存款业务、贷款帐务、卡业务、支付结算等临柜业务。\n'
          },
          {
            did: '2',
            name: '卡交换平台',
            systemNumber: '1201',
            systemStatus: '已下线',
            sysniche: '卡交换平台主要负责银联银行卡交易的数据交换、交易识别、协议转发和ATM、POS设备资料、密钥分发、参数控制、系统监控、商户收单、系统信息维护、机构签到（退）、数据备份、收单商户信息的登记以及银联交易的安全控制和管理。遵循银行卡联网安全规范，并提供对外接口。'
          }
        ]
      }
    },

    components: {
      'my-component-card': Card
    },

    methods: {
      handleChange (el) {
        let current = el.mp.detail.key
        this.current = current
      }

    }
  }
</script>

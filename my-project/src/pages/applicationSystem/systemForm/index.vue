<template>
  <view>
    <i-panel title="基础用法">
      <i-input :value="formData.name" title="系统名称" autofocus placeholder="系统名称" />
      <i-input :value="formData.name" type="number" title="系统编号" placeholder="请输入系统编号" disabled />
      <i-input :value="formData.systemStatus"  title="系统状态" placeholder="请选择系统状态"  />
      <i-input :value="formData.sysniche" title="系统概述" type="textarea" maxlength="50" />
    </i-panel>
  </view>
</template>

<script>
  export default {
    props: [
      'formData',
      'current'
    ],
    methods: {
    }
  }
</script>

<style>
</style>

<template>
  <div>
    <i-tab-bar :current="current" :fixed=true @change="handleChange">
      <i-tab-bar-item key="brush" icon="brush" current-icon="brush_fill" title="草稿"></i-tab-bar-item>
      <i-tab-bar-item key="task" icon="task" current-icon="task_fill" title="待审核"></i-tab-bar-item>
      <i-tab-bar-item key="undo" icon="undo" current-icon="undo" count="3" title="被驳回"></i-tab-bar-item>
      <i-tab-bar-item key="success" icon="success" current-icon="success_fill" title="审核通过"></i-tab-bar-item>
    </i-tab-bar>
  </div>
</template>

<script>
  export default {
    data () {
      return {
        current: 'brush'
      }
    },

    components: {},

    methods: {
      handleChange (el) {
        let current = el.mp.detail.key
        this.current = current
        // switch (current) {
        //   case "brush"
        //   case "task"
        //   case "undo"
        //   case "success"
        // }
      }
    }
  }
</script>

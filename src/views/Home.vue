<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png"> -->
    <HelloWorld :configJsonArr="configJson"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/Config.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld
  },
  data () {
    return {
      configJson: [{
        type: 'Input',
        props: {
          placeholder: '我是默认值',
          clearable: true
        }
      }, {
        type: 'Select',
        props: {
          placeholder: '我是默认值'
        }
      }, {
        type: 'Input',
        props: {
          placeholder: '我是默认值',
          suffixIcon: 'el-icon-delete'
        }
      }]
    }
  }
}
</script>

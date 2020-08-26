<template>
  <div class="hello">
    <div v-for="(config, index) in configJsonArr" :key="config.type + index">
      <!-- <component :is="config.type" :configProps="config.props"></component> -->
      <comp-form-item :configJson="config"></comp-form-item>
    </div>
  </div>
</template>

<script>
import Input from './Input'
import Select from './Select'

const CompFormItem = {
  components: {
    Input, Select
  },
  name: 'FormItem',
  props: {
    configJson: {
      required: true
    }
  },
  render (h) {
    return h(`${this.configJson.type}`, {
      props: {
        ...this.configJson.props || {}
      },
      attrs: {
        ...this.configJson.props || {}
      }
    })
  }
}

export default {
  name: 'Config',
  components: {
    // Input,
    // Select,
    CompFormItem
  },
  props: {
    configJsonArr: {
      type: Array,
      required: true,
      default: () => []
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>

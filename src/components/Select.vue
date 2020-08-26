<template>
  <div class="hello select-con">
    <label>选择框：</label>
    <el-select v-bind="$attrs" v-model="value"></el-select>
  </div>
</template>

<script>
export default {
  name: 'Select',
  data () {
    return {
      value: ''
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.select-con {
  margin: 20px;
  display: flex;
  align-items: center;
  label {
    width: 170px;
  }
}
</style>

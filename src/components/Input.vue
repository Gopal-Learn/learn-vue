<template>
  <div class="hello input-con">
    <label>输入框：</label>
    <el-input v-bind="$attrs"></el-input>
  </div>
</template>

<script>
export default {
  name: 'Input'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.input-con {
  margin: 20px;
  display: flex;
  justify-content: center;
  align-items: center;
  label {
    width: 200px;
  }
}
</style>

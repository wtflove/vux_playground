<template>
  <div id="app">
    <router-view></router-view>
  </div>
</template>
<script>
export default {
  name: 'app'
}

</script>
<style lang="less">
@import '~vux/src/styles/reset.less';

body,
html {
  height: 100%;
  width: 100%;
}

body {
  color: #3b3b3b;
  /*font-size: 1.618rem;*/
}

html {
  box-sizing: border-box;
  font-size: 10px;
}

</style>

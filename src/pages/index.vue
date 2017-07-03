<template>
  <div class="c-index">
    <router-link to="/foo" class="go">获取更多</router-link>
  </div>
</template>
<script>
export default {
  data() {
    return {
      x: 'index'
    };
  }
};
</script>

<style lang='scss' scoped>
@import '../assets/scss/common.scss';

.c-index {
  position: relative;
  height: 768px;
}

.go {
  color: #555;
  font-size: 26px;
  text-align: center;
  text-decoration: none;
  background-color: white;
  display: block;
  margin: 15px auto;
  padding: 10px;
  width: 200px;
  letter-spacing: 3px;
  @include box-shadow(0 1px 3px $color_shadow1);
}
</style>

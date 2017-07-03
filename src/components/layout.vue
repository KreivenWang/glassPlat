<template>
  <div id="app">
    <div class="apphead">
      <div class="apphead__wrap">
        <div class="apphead__brand">
          供水平台测试
        </div>
        <div class="apphead__nav"></div>
      </div>
    </div>
    <router-view></router-view>
    <div class="appfoot">
      <div class="appfoot__wrap">
        2017 &copy; Kreiven.Mistel - Powered by <b>Vue</b>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      x: 'world'
    };
  }
};
</script>

<style lang='scss'>
@import '../assets/scss/common.scss';

$h_nav: 80px;
$h_nav_ele: 50px;
$mg_nav_ele: 10px;
$h_foot:30px;

html {
  background: #eee;
}

#app {
  font-family: 'Microsoft YaHei', Helvetica, Arial, sans-serif;
  margin: 0 auto;
}

.apphead {
  background-color: $color_white1;
  @include box-shadow(0 1px 3px $color_shadow1);
  @at-root #{&}__wrap {
    position: relative;
    width: 90%;
    margin: 0 auto;
    height: $h_nav;
  }
  @at-root #{&}__brand {
    margin: {
      left: $mg_nav_ele;
    }
    position: absolute;
    height: $h_nav;
    background: url('../assets/logo.png') left center no-repeat;
    background-size: $h_nav_ele $h_nav_ele;
    text-indent: $h_nav_ele+$mg_nav_ele;
    line-height: $h_nav;
  }
  @at-root #{&}__nav {
    position: absolute;
    right: $mg_nav_ele;
    height: $h_nav_ele;
    top: 50%;
    margin-top: (-$h_nav_ele/2);
    width: 200px;
    background-color: blue;
  }
}

.appfoot {
  background: $color_white1;
  @include box-shadow(0 -1px 3px $color_shadow1);
  @at-root #{&}__wrap {
    height: $h_foot;
    line-height: $h_foot;
    width: 90%;
    margin: 0 auto;
    text-align: center;
  }
}
</style>

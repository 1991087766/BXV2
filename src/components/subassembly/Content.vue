<template>
  <div id="content">
    <router-view></router-view>
  </div>
</template>

<script type="text/javascript">
export default {
  name:"content"
}
</script>

<style scoped>
#content{
  width: auto;
  height: auto;
  background-color: #F8F8FF;
  position: absolute;
  top: 42px;
  left: 129px;
  /*left: 39px;*/
  right: 2px;
  bottom: 2px;
  /*border-radius: 5px;*/
}


</style>

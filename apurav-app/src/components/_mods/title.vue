<!-- CopyRight (C) 2017-2022 Alibaba Group Holding Limited. -->
<!-- Created by Tw93 on 17/07/28. -->

<template>
  <div class="wxc-title" :aria-hidden="true">
    <image class="logo" src="http://via.placeholder.com/550x250"></image>
  </div>
</template>

<style scoped>
  .wxc-title {
    margin-top: 20px;
    height:78px;
    flex-direction: row;
    align-items: center;
  }

  .logo {
    margin-left: 24px;
    width: 92px;
    height: 29px;
  }

  .text {
    font-size: 30px;
    font-weight: 600;
    color: #000000;
  }

</style>

<script>
  export default {
    props: {
      title: String
    }
  }
</script>

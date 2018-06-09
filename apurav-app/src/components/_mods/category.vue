
<template>
  <div class="category">
    <text class="category-text">{{title}}</text>
  </div>
</template>

<style scoped>
  .category {
    margin-top: 20px;
    padding-left: 24px;
    width: 750px;
    height: 98px;
    background-color: #f3f7f8;
    justify-content: center;
  }

  .category-text {
    color: #000000;
    font-weight: 600;
    font-size: 28px;
  }

</style>

<script>
  export default {
    props: {
      title: String
    }
  }
</script>

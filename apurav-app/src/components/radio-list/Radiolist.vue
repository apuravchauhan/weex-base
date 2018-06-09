<!-- CopyRight (C) 2017-2022 Alibaba Group Holding Limited. -->
<template>
  <div class="wxc-demo">
    <scroller class="scroller">
      <title title="Logo"></title>
      <category title="Select an option to pay"></category>
      <wxc-radio :list="list" :config="config"
                 @wxcRadioListChecked="wxcRadioListChecked"></wxc-radio>
    </scroller>
  </div>
</template>

<style scoped>
  .wxc-demo {
    position: absolute;
    top: 0;
    right: 0;
    left: 0;
    bottom: 0;
    background-color: #ffffff;
  }

  .scroller {
    flex: 1;
  }

  .radio-text {
    font-size: 30px;
    color: #333333;
    margin-top: 30px;
    margin-bottom: 30px;
    margin-left: 24px;
  }
</style>

<script>
  import Title from '../_mods/title.vue';
  import Category from '../_mods/category.vue';
  import WxcRadio from '../wxc-radio';
  import { setTitle } from '../_mods/set-nav';

  export default {
    components: { Title, Category, WxcRadio },
    data: () => ({
      list: [
        { title: 'Paytm Payments Bank', value: 1 },
        { title: 'Paytm Postpaid', value: 2, checked: true },
        { title: 'Debit Card', value: 3 },
        { title: 'Credit Card', value: 4 },
        { title: 'Net Banking', value: 5 },
        { title: 'EMI', value: 6 }
      ],
      config:{
        checkedColor: '#000000'
      },
      checkedInfo: { title: 'Paytm Postpaid', value: 2, oldIndex: -1, index: 1 }
    }),
    created () {
      setTitle('Radio');
    },
    methods: {
      wxcRadioListChecked (e) {
        this.checkedInfo = e;
      }
    }
  }
</script>

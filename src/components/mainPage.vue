<template>
  <div class="mainPage">
    <div :is="select[isActive]"></div>
  </div>
</template>

<script>

import select1 from '../components/selectPage/select1.vue'
import select2 from '../components/selectPage/select2.vue'
import select3 from '../components/selectPage/select3.vue'
import select4 from '../components/selectPage/select4.vue'

export default {
  name:'mainPage',
  data(){
    return{
      select :[
        'select1',
        'select2',
        'select3',
        'select4'
      ]
    }
  },
  props: {
    isActive:{
      type: Number,
      default: 0
    }
  },
  components: {
    select1,
    select2,
    select3,
    select4
  },
  compled: {

  },
  watch: {
    isActive(val){
      console.log(val);
    }
  }
}
</script>
<style lang="less" scoped>

</style>

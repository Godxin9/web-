<template>
  <div>
    <div>
          <TextShow v-for="(item,index) in contexts" :key="index" :title="item.title" :context="item.context" @delteComment="delteComments" :index="index"/>
    </div>
    <!-- <TextShow v-for="(item,index) in contexts" :key="index" :title="item.title" :context="item.context"/> -->
  </div>
</template>

<script>
import TextShow from '@/components/text'
export default {
  data() {
    return {
      contexts:[
        {title:'嘉然',context:'关注嘉然，顿顿解馋！！'},
        {title:'向晚',context:'顶碗人！！'},
        {title:'珈乐',context:'皇珈骑士！！'},
        {title:'贝拉',context:'贝极星！！'},
        {title:'乃琳',context:'乃淇淋！！'},
      ]
    }
  },
  components:{
    TextShow
  },
  methods:{
    // delteText(index){
    //   this.contexts.splice(index,1)
    // }
    delteComments(index){
      this.contexts.splice(index,1)
    }
  }
}
</script>

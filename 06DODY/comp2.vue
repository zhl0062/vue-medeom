<template>
  <div>
    <!-- // 把数据传给子组件 -->
    <!-- 2.在父组件中自定义一个属性=创建方法的函数名 -->
    <p>{{ fathernum}}</p>
   <child :num="fathernum" @fn1="clickres1" @fn2="clickres2"></child>
  </div>
</template>
<script>
// 2.调用子组件
import child from './comp2child.vue'
export default {
data:function(){
    return{
        // 定义父组件数据
        fathernum:20
    }
},
// 1.在父组件中创建一个方法
methods:{
clickres1:function(val){
this.fathernum++
},
clickres2:function(val){
this.fathernum--
},
},
// 1.注册子组件
components:{
    child
}
}
</script>

<style>

</style>
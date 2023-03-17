<template>
  <div>
    <h1>这是子组件</h1>
    <h1>{{ num }}</h1>
    <button @click="but1">按钮+</button>
    <button @click="but2">按钮-</button>
  </div>
</template>

<script>
export default {
    // 接收父组件的数据
    props:['num'],
data:function(){
    return{

    }
},
methods:{
    but1:function(){
// 3.在子组件中通过this.$emit()来触发自定义事件，从而执行父组件方法里的函数
        this.$emit('fn1')
    },
but2:function(){
    this.$emit('fn2')
}
}
}
</script>

<style>

</style>
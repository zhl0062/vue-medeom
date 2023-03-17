<template>
  <div>
    <h1>这是一个组件</h1>
    <h1>{{ num}}</h1>
    <button @click="but">按钮</button>
  </div>
</template>

<script>
export default {
data:function(){
    return {
        num:20
    }
},
methods:{
    but:function(){
        this.num++
    }
}

}
</script>

<style>

</style>
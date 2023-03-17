<template>
    <div>
        <h1>我是子组件</h1>
    </div>
</template>

<script>
export default {
    data () {
        return {
          num:200  
 
        }
    },
    methods:{
        child:function(){
            console.log('这是子组件的方法');
        }
    }
}
</script>
 
<style lang = "less" scoped>
    
</style>
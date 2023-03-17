<template>
    <div>
        <h1>{{num }}</h1>
        <button @click="but">点击按钮++</button>
    </div>
</template>

<script>
export default {
    data () {
        return {
            num:100
 
        }
    },
    methods:{
        but:function(){
            this.num++
        }
    },
    // watch 属性监听，监听某些属性被修改的值
    watch:{
        // // 第一种格式
        // // nuwval 新修改了的值 ，olbval之前还未被修改的值
        // num:function(nuwval,olbval){
        //     console.log('num被修了',nuwval,olbval);
        // },

                // 第二种格式
        num:{
            handler:function(numval,oldval){
                console.log('num被修改了',numval,oldval);
            }
        }
    }
}
</script>
 
<style lang = "less" scoped>
    
</style>
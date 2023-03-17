<template>
    <div>
        <!-- ref属性标签和$refs对象 -->
        <h1 ref="op">我是h1</h1>
        <button @click="but">点击改变颜色</button>
        <!--调用子组件 -->
        <child ref="op2"></child>
   </div>
</template>

<script>
import child from "./comp7child.vue"
export default {
    data () {
        return {

 
        }
    },
    // 注册子组件
    components:{
        child
    },
    methods:{
        but:function(){
            // this.$refs对象，专门来接收这个组件中带有ref的属性的标签/子组件，作为自己的属性
            console.log(this.$refs.op.innerHTML);
            // ref="属性名--op"
            this.$refs.op.style.color='#bfa'
            // 调用子组件中的方法
            console.log(this.$refs.op2.num);
            this.$refs.op2.child()
        }
    }
}
</script>
 
<style lang = "less" scoped>
    
</style>
<template>
    <!-- 生命周期 -->
    <div>
        <h1 ref="op">{{ num }}</h1>
        <button @click="but">按钮++</button>
    </div>
</template>

<script>
export default {
    data () {
        return {

            num:20
        }
    },
    methods:{
        but:function(){
         this.   num++
        }
    },
    // 1.初始化阶段:(创建期)  把数据和方法初始化，挂到对象上
//   实例刚刚在内存中被创建出来，此时还没有初始化 `data` 和 `methods` 属性
    beforeCreate:function(){
        console.log("beforeCreate",this.num,this.but,this.$refs.op);
    },
    // 实例已经在内存中创建好，此时 `data`和`methods` 已经创建好，此时还没有开始编译模板
    //
    created:function(){
        console.log("created",this.num,this.but,this.$refs.op);
    },

    // 2.挂载阶段 ：(挂载期)--模板准备好后把数据填到模板上
     // 此时已经完成了模板编译，但是还没有挂载到页面中；
    beforeMount:function(){
        console.log("beforeMount",this.num,this.but,this.$refs.op);
    },
//    这个时候已经把编译好的模板挂载到页面指定的容器里；
    mounted:function(){
        console.log("mounted",this.num,this.but,this.$refs.op);
    }

}
</script>
 
<style lang = "less" scoped>
    
</style>
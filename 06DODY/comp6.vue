<template>
    <div>
        <h1>{{ num }}</h1>
        <button @click="but">点击按钮++</button>

        <!-- 深度监听 -->
        <h1>{{ obj.age }}</h1>
        <button @click="but2">点击按钮++</button>
    </div>
</template>

<script>
export default {
    data () {
        return {
            num:200,
            obj:{
                name:'欧阳修',
                age:100
            }
        }
    },
    methods:{
        but:function(){
            this.num++
        },
        but2:function(){
            this.obj.age++
        }
    },
    watch:{
        // 立即监听

        // num:{
        //     handler:function(numval,oldval){
        //         console.log('num值被修改为',numval,oldval);
        //     },
        //     immediate:true //表示页面一刷新就监听  
        // }

        // 深度监听 --指定监听到某个属性
        'obj.age':{
            handler:function(numval,oldval){
                // age 的值被修改的时候执行
                console.log('age值改为',numval,oldval);
            }
        }
    }
}
</script>
 
<style lang = "less" scoped>
    
</style>
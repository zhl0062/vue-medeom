<template>
    <div>
        <!-- 事件修饰符
        .stop  表示可以阻止事件冒泡
        .prevent 表示可以阻止浏览器的默认行为
        .once 只让事件触发一次，后面都不触发了
    -->
        <div class="box1" @click="but1">
            <div class="box2" @click.stop="but2">
            <a href="#" @click.stop.prevent>这是a标签</a>
            </div>
        </div>
        <button @click.once="bun3">点击抢优惠价</button>
  
        <!-- 按键修饰符 -->
        <!-- .enter  表示回车发布 -->
        <input type="text" @keyup.enter="hdkeyup">
  </div>
</template>

<script>
export default {
    data () {
        return {

 
        }
    },
    methods:{
        hdkeyup:function(){
            console.log('ok');
        },
        but1:function(){
            console.log('这是box1');
        },
        but2:function(){
            console.log('这是box2');
        },
        bun3:function(){
            console.log('恭喜你没有抢到');
        }
    }
}
</script>
 
<style lang = "less" scoped>
    .box1{
        width: 300px;
        height: 300px;
       background-color: red;
    }
    .box2{
        width: 150px;
        height: 150px;
        background-color: #bfa
    }
</style>
<template>
    <div>
        <!-- 表单修饰符 
        .trim 在获取到用户输入的文本之前 去掉空格-->
        <input type="text" v-model.trim="textval">
        <button @click="but">按钮</button>
        <br>
        <!--.number 在获取用户输入的数字之后自动转成数字类型 -->
        <input type="number" v-model.number="numval">
        <button @click="but2">按钮2</button>
        <br>
        <!-- .lazy 等回车或失焦的时候才会更新用户输入的数据 -->
        <input type="text" v-model.lazy="textval2">
        <p>{{textval2}}</p>
    </div>
</template>

<script>
export default {
    data () {
        return {
            textval:'',
            numval:null,
            textval2:''
 
        }
    },
    methods:{
        but:function(){
            if(this.textval==''){
                alert('请输入文字')
                return
            }
        },
        but2:function(){
            console.log(this.numval)
        }

    }
}
</script>
 
<style lang = "less" scoped>
    
</style>
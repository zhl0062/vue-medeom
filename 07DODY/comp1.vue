<template>
    <div>
        <div class="top">
            <span>名称</span>
            <input type="text"> 
            <button>查询</button>
        </div>
        <table>		
            <tr>		
                <th v-for="item in titxt" :key="item.id">{{ item }}</th>
            </tr>		
            <tr v-for="text,index in arr" :key="text">
                <td>{{ text.shux }}</td>
                <td>{{ text.textval}}</td>
                <td>{{ text.num .toFixed(2)}}</td>
                <td>
                    <button @click="but(index)">{{ text. but}}</button>
                </td>
            </tr>


            <tr class="trc">
                <td  colspan="6">总价为:{{ total }}</td>
            </tr>
        </table>
    </div>
</template>

<script>
export default {
    data () {
        return {
            titxt:['ID','主标题','起步价','操作'],
            arr:[
                {
                    shux:287,
                    textval:"严选新式样板间",
                    num:29.9,
                    but:'删除'
                },
                {
                    shux:286,
                    textval:"无“油”无虑的甜蜜酥脆",
                    num:45,
                    but:'删除'
                },
                {
                    shux:283,
                    textval:"孩子成长中少不了的一双鞋",
                    num:888,
                    but:'删除'
                },
                {
                    shux:282,
                    textval:"成就一室米香",
                    num:78,
                    but:'删除'
                },
                {
                    shux:281,
                    textval:"条纹新风尚",
                    num:29,
                    but:'删除'
                },
                {
                    shux:277,
                    textval:"治愈生活的满怀柔软",
                    num:66.78,
                    but:'删除'
                },
                {
                    shux:274,
                    textval:"没有软木托,怎么过冬天",
                    num:50.99,
                    but:'删除'
                },
                {
                    shux:272,
                    textval:"料理也要精细简单",
                    num:69,
                    but:'删除'
                },
                {
                    shux:268,
                    textval:"新式懒人",
                    num:15.3,
                    but:'删除'
                },

            ]
 
        }
    },
    // 计算属性
    computed:{
        total:function(){
         let res= this.arr.reduce((per,cur)=>{
                return per+cur.num
            },0)
            return '￥'+res.toFixed(2)+'元'
            
        }
    },
    // 方法
    methods:{
        but:function(index){
            this.arr.splice(index,1)
        }
    }

}
</script>
 
<style lang = "less" scoped>
            *{margin: 0;padding: 0;}
        body{font-size: 14px; color:#666; padding-left: 50px;padding-top: 30px;}
        input,button{outline-style: none;}
        table{border: 1px solid #ddd;border-collapse: collapse; }
        td,th{border: 1px solid #ddd; width: 150px; height: 30px;text-align: left; padding: 10px;}
        .top{   
            display: flex;
            margin-bottom: 10px;
        }
        .top>*{
            margin-right: 20px;
        }
        .top span{
            line-height: 40px;
        }
        .top input{
            border:1px solid #ccc;
            border-radius:4px;
            padding-left: 8px;
            color:#666;
        }
        button{
            border:0;
            padding:10px 15px; background-color: skyblue;
            color:#fff;
            border-radius:4px;
        }
        trc{
            text-align:left
        }
</style>
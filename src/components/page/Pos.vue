<template>
    <div class="pos">
        <el-row>
            <el-col :span="7" class="pos-order" id="order-list">
                我是订单栏
            </el-col>
            <el-col :span="17">
                我是产品栏
            </el-col>

        </el-row>
    </div>
</template>
<script>
export default {
    name: 'pos',
    //查看技术胖的生命周期， mounted的意思就是当所有的虚拟dom加载完成之后它要执行的方法。
    mounted:function(){
        var orderHeight=document.body.clientHeight;
        console.log(orderHeight);
        document.getElementById('order-list').style.height=orderHeight+'px';
    },
    data() {
        return {
        };
    }
}
</script>
<style lang="css" scoped>
.pos-order{
    background-color: #f9fafc;
    border-right: 1px solid #c0ccda;
}
</style>
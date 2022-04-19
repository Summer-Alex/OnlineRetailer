<template>
    <div>
        <div class="top">
            <font-awesome-icon icon="fa-solid fa-arrow-left" @click="routeBack()"  class="icon"/>
            <span class="msg">商品详情</span>
        </div>
        <div class="manage">
            <span class="number">全部宝贝 2件</span>
            <span class="right">管理</span>
        </div>
            <div class="example">
                <img src="@/assets/img/cart/资源 96.png" alt="">
                <div>
                    <div class="msg">
                        <span>2022 苗族土家族湘西舞蹈服装苗家舞蹈装</span>
                    </div>
                    <span class="color">墨绿色</span>
                    <div class="money">
                        <font-awesome-icon icon="fa-solid fa-yen-sign" /><span>300.00</span>
                        <el-input-number v-model="num" :min="1" :max="10" label="数量"></el-input-number>
                    </div>
                </div>
            </div>
            <div class="example">
                <img src="@/assets/img/cart/资源 97.png" alt="">
                <div>
                    <div class="msg">
                        <span>花边辅料领口袖口服苗家舞台装饰品配件苗族风布料条</span>
                    </div>
                    <span class="color">苗族格子款</span>
                    <div class="money">
                        <font-awesome-icon icon="fa-solid fa-yen-sign" /><span>20.00</span>
                        <el-input-number v-model="num" :min="1" :max="10" label="数量"></el-input-number>
                    </div>
                </div>
            </div>
    </div>
</template>


<script>
export default {
    data(){
        return{
            num:1,
        }
    },
    components:{

    },
    methods:{
        routeBack(){
            this.$router.push('/shop')
        }
    }
}
</script>


<style scoped lang="scss">
.top{
background-color: rgb(250, 241, 241);    
height: 90px;
font-size: 40px;
display: flex;
justify-content: center;
align-items: center;
position: relative;
    .icon{
        position: absolute;
        left: 20px;
    }
}
.manage{
    display: flex;
    color: rgb(194, 194, 194);
    margin-left: 30px;
    margin-right: 30px;
    padding-left: 10px;
    padding-right: 10px;
    font-size: 25px;
    align-items: center;
    height: 70px;
    border-bottom: 3px rgb(235, 209, 209) solid;
    .right{
        margin-left: auto;
    }
}
.example{
    display: flex;
    height: 230px;
    margin-left: 30px;
    margin-right: 30px;
    border-bottom: 3px rgb(235, 209, 209) solid;
    align-items: center;
    padding-left: 30px;
    padding-right: 30px;
    flex-wrap: wrap;
    img{
        width: 180px;
        height: 180px;
    }
    .msg{
        width: 420px;
        font-size: 30px;
        font-weight: lighter;
        margin-left: 20px;
    }
    .color{
        margin-left: 20px;
        display: inline-block;
        color: rgb(177, 177, 177);
        font-size: 23px;
        padding-top: 10px;
    }
    .money{
        margin-left: 20px;
        color:rgb(235, 101, 101); ;
        display: flex;
        align-items: center;
        font-size: 30px;
        padding-top: 5px;

    }
}
</style>

<style scoped>
::v-deep .el-input-number{
    margin-left: auto;
}
</style>
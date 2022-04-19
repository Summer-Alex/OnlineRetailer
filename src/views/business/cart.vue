<template>
    <div>
        <div class="top">
            <span class="msg">订单信息</span>
        </div>    
        <div class="title">
            待发货
        </div>
                <div class="example">
                    <img src="@/assets/img/information/资源 43.png" alt="">
                    <div>
                        <div class="msg">
                            <span>2021新款韩服表演服饰女宫廷传统舞蹈服装民族古装成人朝鲜族服装</span>
                        </div>
                        <span class="color">中号M</span>
                        <div class="money">
                            <font-awesome-icon icon="fa-solid fa-yen-sign" /><span>120.00</span>
                            <span class="right">yq12345买家已付款</span>
                        </div>
                    </div>
                </div>
                 <div class="example">
                    <img src="@/assets/img/information/资源 44.png" alt="">
                    <div>
                        <div class="msg">
                            <span>少数民族复古潮品时尚民族风耳饰女流苏气质耳环藏银耳坠百搭配饰</span>
                        </div>
                        <span class="color">套餐A</span>
                        <div class="money">
                            <font-awesome-icon icon="fa-solid fa-yen-sign" /><span>40.10</span>
                            <span class="right">yq12345买家已付款</span>
                        </div>
                    </div>
                </div>
                 <div class="example">
                    <img src="@/assets/img/information/资源 45.png" alt="">
                    <div>
                        <div class="msg">
                            <span>少数民族复古潮品时尚民族风耳饰女流苏气质耳环藏银耳坠百搭配饰</span>
                        </div>
                        <span class="color">套餐B</span>
                        <div class="money">
                            <font-awesome-icon icon="fa-solid fa-yen-sign" /><span>31.10</span>
                            <span class="right">yq12345买家已付款</span>
                        </div>
                    </div>
                </div>
        <div class="title">
            待退款
        </div>
                 <div class="example height">
                    <img src="@/assets/img/information/资源 45.png" alt="">
                    <div>
                        <div class="msg">
                            <span>花边辅料领口袖口服苗家舞台装饰品配件苗族风布料条</span>
                        </div>
                        <span class="color">123</span>
                        <div class="money">
                            <font-awesome-icon icon="fa-solid fa-yen-sign" /><span>10.00</span>
                            <span class="right">yq12345买家申请退款</span>
                        </div>
                    </div>
                </div>        
    </div>
</template>


<script>
export default {
    data(){
        return{

        }
    },
    methods:{
        routeBack(){
            this.$router.push('/myPage')
        }
    },
    components:{

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
.title{
    margin-left: 40px;
    font-size: 25PX;
    margin-top: 20px;
    font-weight: lighter;
}
.height{
    margin-bottom: 100px;
}
.example{
    display: flex;
    height: 330px;
    margin-top: 20px;
    border-radius: 20px;
    margin-left: 30px;
    margin-right: 30px;
    background-color: rgb(249, 240, 240);
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
    .right{
        margin-left: auto;
        font-weight: lighter;
    }
    .click{
        width: 100%;
        display: flex;
        justify-content: space-between;
        button{
            border: rgb(242, 170, 170)  3px solid;
            outline: none;
            background-color:rgb(249, 240, 240);
            width: 150px;
            height: 60px;
            border-radius: 20px;
            font-size: 25px;
        }
    }
}
</style>
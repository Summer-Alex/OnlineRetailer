<template>
    <div>
        <div class="top">
            <img src="@/assets/img/主界面/资源 12.png" alt="" class="icon">
            <span class="msg">陈小姐的店</span>
        </div>
        <div class="money">
            <h3 class="deal">今日成交额(元)</h3>
            <div class="detail">
                <span class="number">2960.00</span>
                <span class="compare"><font-awesome-icon icon="fa-solid fa-arrow-up-long" /><span class="up">较昨日有所上升</span></span>
            </div>
            <ul>
                <li>今日访客</li>
                <li>今日新增粉丝</li>
                <li>今日订单</li>
            </ul>
            <ul>
                <li>100</li>
                <li>40</li>
                <li>88</li>
            </ul>
        </div>
        <ul class="goods">
            <li><span>待发货</span><span  class="title line">66</span></li>
            <li><span>待退货</span><span  class="title">10</span></li>
        </ul>  
        <div class="container">
            <div class="example">
                <img src="@/assets/img/主界面/资源 3.png" alt="">
                <span class="explain">店铺管理</span>
            </div>
            <div class="example">
                <img src="@/assets/img/主界面/资源 3.png" alt="">
                <span class="explain">商品管理</span>
            </div>
            <div class="example">
                <img src="@/assets/img/主界面/资源 4.png" alt="">
                <span class="explain">库存管理</span>
            </div>
            <div class="example">
                <img src="@/assets/img/主界面/资源 5.png" alt="">
                <span class="explain">运营数据</span>
            </div>
            <div class="example">
                <img src="@/assets/img/主界面/资源 6.png" alt="">
                <span class="explain">店铺营收</span>
            </div>
            <div class="example">
                <img src="@/assets/img/主界面/资源 7.png" alt="">
                <span class="explain">优惠管理</span>
            </div>
        </div>   
    </div>
</template>



<script>
// import businessNav from "@/components/businessNav.vue"
export default {
    data(){
        return{

        }
    },
    methods:{

    },
    components:{
        // businessNav
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
    left: 30px;
}
}
.money{
    background-color: rgb(235, 101, 101);
    width: 650px;
    height: 350px;
    border-radius: 25px;
    margin: 25px auto;
    color: white;
    box-sizing: border-box;
    .deal{
      display: inline-block;
      margin-top: 80px;
      font-size: 17PX;
      font-weight: lighter;
      letter-spacing: 1.5px;
      padding-left: 40px;
    }
    .detail{
        margin-top: 30px;
        padding-left: 40px;
        margin-bottom: 40px;
        .number{
            font-size: 28PX;
        }
        .compare{
            margin-left: 30px;
            font-size: 24PX;
        }
        .up{
            color: rgb(207, 207, 207);
            font-size: 12px;
            margin-left: 10px;
        }
    }
    ul{
        display: flex;
        justify-content: space-between;
        margin-top: 10px;
        color: white !important;
        li{
            display: flex;
            width: 150px;
            justify-content: center;
        }
    }
}
.goods{
    margin-top: 80px;
    display: flex;
    align-items: center;
    height: 100px;
    border-radius: 15px;
    border: 2px solid rgb(255, 193, 193);
    margin-left: 50px;
    margin-right: 50px;
    li{
        display: flex;
        align-items: center;
        width: 50%;
        margin-left: 30px;
        font-size: 30px;
        font-weight: lighter;
        .title{
            margin-left: auto;
            padding-right: 30px;
            height: 80px;
            display: flex;
            align-items: center;
        }
        .line{
            box-sizing: border-box;
            border-right:2px solid rgb(255, 193, 193);
        }
    }
}
.container{
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    margin: 0 auto;
    width: 650px;
    .example{
        width: 180px;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-wrap: wrap;
        margin-top: 60px;
        img{
            width:100px;
        }
        .explain{
            font-size: 17PX;
            display: inline-block;
            margin-top: 30px;
        }
    }
}
</style>



<style scoped>

</style>
<template>
    <div>
        <div id="background"></div>
        <ul class="icon">
            <li><img src="@/assets/img/吾/资源 68.png" alt=""></li>
            <li @click="routerToCommunicate()"><img src="@/assets/img/吾/资源 69.png" alt=""></li>
            <li><img src="@/assets/img/吾/资源 70.png" alt=""></li>
        </ul>
        <div class="user">
            <img src="@/assets/img/吾/资源 71.png" alt="">
            <ul>
                <li class="name">村村<font-awesome-icon icon="fa-solid fa-venus" class="woman" :transform="{ rotate: 42 }" /></li>
                <li class="level">乐师10级</li>
            </ul>
            <div class="positon" @click="routerToCoin()">
                <div class="number">
                    <span>乐师积分:300</span>
                </div>
                <div class="number">
                    <span>乐师币:3000</span>
                </div>
            </div>
        </div>
         <ul class="rank">
            <li><span class="border"><img src="@/assets/img/吾/资源 72.png" alt=""></span><span>签到</span></li>
            <li><span class="border"><img src="@/assets/img/吾/资源 73.png" alt=""></span><span>历史记录</span></li>
            <li><span class="border"><img src="@/assets/img/吾/资源 74.png" alt=""></span><span>下载</span></li>
            <li><span class="border"><img src="@/assets/img/吾/资源 75.png" alt=""></span><span>收藏</span></li>
        </ul>
        <div class="put" @click="routerToContribute()">
            <span>点击这里发现投稿区哦~</span>
        </div>
        <div class="service">
            <span class="title">更多服务</span>
            <div class="container">
                    <img src="@/assets/img/吾/资源 76.png" alt="">
                    <span class="detail">联系我们</span>
                <img src="@/assets/img/吾/资源 80.png" alt="" class="right">
            </div>
             <div class="container" @click="routerToShopImformation()">
                    <img src="@/assets/img/吾/资源 77.png" alt="">
                    <span class="detail">订单信息</span>
                <img src="@/assets/img/吾/资源 80.png" alt="" class="right">
            </div>
             <div class="container">
                    <img src="@/assets/img/吾/资源 78.png" alt="">
                    <span class="detail">意见与反馈</span>
                <img src="@/assets/img/吾/资源 80.png" alt="" class="right">
            </div>
             <div class="container">
                    <img src="@/assets/img/吾/资源 79.png" alt="">
                    <span class="detail">设置</span>
                <img src="@/assets/img/吾/资源 80.png" alt="" class="right">
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
        routerToCoin(){
            this.$router.push('/coin')
        },
        routerToContribute(){
            this.$router.push('/contribute')
        },
        routerToShopImformation(){
            this.$router.push('/shopImformation')
        },
        routerToCommunicate(){
            this.$router.push('/communicate')
        }
    }
}
</script>

<style scoped lang="scss">
.icon{
    height: 100px;
    display: flex;
    justify-content: flex-end;
    margin-right: 70px;
    align-items: center;
    li{
        margin-left: 20px;
    }
}
.user{
    background: linear-gradient(white,rgb(255, 235, 229));
    display: flex;
    height: 250px;
    padding-left: 70px;
    box-sizing: border-box;
    position: relative;
    img{
        width: 130px;
        height: 130px;
    }
    ul{
        font-size: 40px;
        margin-left: 40px;
        li{
            margin-top: 10px;
        }
       .name{
           margin-left: 20px;
            .woman{
            color: rgb(222, 99, 97);
            margin-left: 20px;
            font-size: 30px;
            font-weight: lighter;
        }
       }
        .level{
            font-size: 25px;
            box-sizing: border-box;
            color: white;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 10px;
            padding-top: 5px;
            padding-bottom: 5px;
            width: 120px;
            
            background-color: rgb(243,160,151);
        }
    }
    .positon{
        position: absolute;
        bottom: 10px;
        display: flex;
        .number{
            margin-left: 40px;
            background-color: rgb(238,125,120);
            color: white;
            width: 250px;
            height: 75px;
            border-radius: 15px;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 28px;
        }
    }
}
.rank{
    display: flex;
    justify-content: space-around;
    height: 150px;
    margin-top: 20px;
    li{
        width: 120px;
        height: 50px;
        font-size: 16PX;
        display: flex;
        flex-wrap: wrap;
        align-items: center;
        justify-content: center;
        .border{
            border-radius: 50%;
            width: 90px;
            height: 90px;
            display: flex;
            justify-content: center;
            align-items: center;
            margin-bottom: 5px;
        }
        img{
            width: 60px;
            height: 60px;
        }
    }
}
.put{
    display: flex;
    align-items: center;
    color: white;
    background-color: rgb(238,125,120);
    height: 90px;
    font-size: 35px;
    border-radius: 20px;
    margin: 30px 60px 0 60px;
    padding-left: 60px;
}
.service{
    margin: 40px 90px 0 70px;
    height: 520px;
    .title{
        font-size: 40px;
        color: rgb(71, 71, 71);
    }
    .container{
        margin-top: 30px;
        display: flex;
        align-items: center;
        .detail{
            color: grey;
            margin-left: 30px;
            font-size: 30px;
        }
        .right{
            margin-left: auto;
            height:40px;
            width: 40px;
        }
        img{
            width: 65px;
            height: 65px;
        }
    }
}
</style>

<style scoped>
#background{
opacity:1;
background-image: url('../../assets/img/吾/资源 35.png');
background-size: cover;
width:100%;
height:100%;
position:fixed;
z-index: -99;
}
</style>
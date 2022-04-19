<template>
    <div>
        <div class="top">
            <font-awesome-icon icon="fa-solid fa-arrow-left" @click="routeBack()"  class="icon"/>
            <span class="msg">商品详情</span>
        </div>
        <img src="@/assets/img/购物车/资源 105.png" alt="" class="imgDetail">
        <div class="detail">
            <img src="@/assets/img/购物车/资源 96.png" alt="" class="goods">
            <div class="condition">
                     <h3 class="money"><font-awesome-icon icon="fa-solid fa-yen-sign" /><span class="money"> 300.00</span></h3>
                    <span class="store">库存200件</span>
            </div>
        </div>
        <div class="comment">
            <img src="@/assets/img/购物车/资源 107.png" alt="">
            <span class="like">100人评论款式很赞！</span>
            <div class="all">
                <span>全部1000+评论</span>
                <img src="@/assets/img/购物车/资源 108.png" alt="">
            </div>
        </div>
        <div class="model">
            <span class="title">款式</span>
            <div class="container">
                <div class="example">
                    <img src="@/assets/img/购物车/资源 110.png" alt="">
                    <span class="color">墨绿色</span>
                </div>
                 <div class="example">
                    <img src="@/assets/img/购物车/资源 111.png" alt="">
                    <span class="color">红色</span>
                </div>
            </div>
        </div>
        <div class="size">
            <span class="title">大小</span>
            <ul>
                <li>S</li>
                <li>M</li>
                <li>L</li>
                <li>XL</li>
                <li>2XL</li>
            </ul>
        </div>
         <div class="model">
            <span class="title">购买数量</span>
        </div>
        <div class="bottom">
            <ul>
                <li><img src="@/assets/img/购物车/资源 112.png" alt="">店铺</li>
                <li><img src="@/assets/img/购物车/资源 113.png" alt="">客服</li>
                <li><img src="@/assets/img/购物车/资源 114.png" alt="">收藏</li>
            </ul>
            <div class="click">
                <button class="add">加入购物车</button>
                <button class="buy">立即购买</button>
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
}
.icon{
    position: absolute;
    left: 20px;
}
.imgDetail{
    width: 100%;
}
.detail{
    display: flex;
    justify-content: center;
    position: relative;
    height: 180px;
    .goods{
        position:absolute;
        top: -90px;
        left: 60px;
        width: 250px;
    }
    .condition{
        margin-left: 80px;
        margin-top: 40px;
        .money{
            color:rgb(235, 101, 101);
            font-size: 40px;
        }
        .store{
            display: inline-block;
            margin-top: 10px;
            font-size: 25px;
        }
    }
}
.comment{
     display: flex;
     margin-left: 30px;
     margin-right: 30px;
     padding-left: 35px;
     border-radius: 15px;
     align-items: center;
     height: 50px;
     background-color: rgb(250, 241, 241);   
     color: grey;
     font-weight: lighter;
     font-size: 25px;
     .like{
         margin-left: 15px;
     }
     .all{
         margin-left: auto;
         margin-right: 20px;
     }
}
.model{
    margin: 15px 40px 0 40px;
    padding-bottom: 20px;
    border-bottom: 2px solid grey;
    .title{
        font-size: 35px;
        font-weight: 600;
        display: inline-block;
        margin-bottom: 10px;
    }
    .container{
        display: flex;
        .example{
            background-color: rgb(250, 241, 241); 
            display: flex;
            margin-left: 30px;
            flex-wrap: wrap;
            width: 200px;
            height: 260px;
            justify-content: center;
            img{
                width: 180px;
            }
            .color{
                margin-top: 15px;
                font-size: 30px;
            }
        }
    }
}
.size{
    margin: 15px 40px 0 40px;
    padding-bottom: 20px;
    border-bottom: 2px solid grey;
    .title{
        font-size: 35px;
        font-weight: 600;
        display: inline-block;
        margin-bottom: 10px;
    }
    ul{
        display: flex;
        li{
            background-color: rgb(250, 241, 241); 
            width: 90px;
            margin-left: 30px;
            height: 50px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 30px;
            border-radius: 15px;
        }
    }    
}
.bottom{
    display: flex;
    height: 100px;
    align-items: center;
    margin-top: 20px;
    padding: 10px 30px;
    background-color: rgb(235, 235, 235);
    border-radius: 0 0 15px 15px;
    ul{
        display: flex;
        li{
            width: 50px;
            margin-left: 45px;
            font-size: 25px;
            img{
                width: 50px;
            }
        }
    }
    .click{
        margin-left: auto;
        button{
            border: none;
            width: 150px;
            height: 70px;
            border-radius: 10px;
            margin-right: 30px;
            outline: none;
            color: white;
            font-size: 25px;
        }
        .add{
            background: linear-gradient(to right,#EABC2A,#E88F24);
        }
        .buy{
             background: linear-gradient(to right,#E26F1F,#DD4D1C);
        }
    }
}
</style>
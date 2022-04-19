<template>
    <div>
        <div class="top">
            <div class="position">
                <img src="@/assets/img/云铺/资源 86.png" alt="" class="glass">
                <input type="text" placeholder="输入关键字"> 
                <img src="@/assets/img/云铺/资源 87.png" alt="" class="camera">
            </div>
            <div class="icon">
                <img src="@/assets/img/云铺/资源 89.png" alt="" @click="routerToshopCart()">
                <img src="@/assets/img/云铺/资源 90.png" alt="" class="bottom">
            </div>
        </div>
        <el-carousel trigger="hover" height="150px" arrow="never">
            <el-carousel-item v-for="item in 4" :key="item">
                <img src="@/assets/img/云铺/资源 91.png" alt="">
            </el-carousel-item>
        </el-carousel>
        <ul class="rank">
            <li><span class="border"><img src="@/assets/img/云铺/资源 92.png" alt=""></span><span>新品专区</span></li>
            <li><span class="border"><img src="@/assets/img/云铺/资源 93.png" alt=""></span><span>爆款</span></li>
            <li><span class="border"><img src="@/assets/img/云铺/资源 94.png" alt=""></span><span>促销</span></li>
            <li><span class="border"><img src="@/assets/img/云铺/资源 95.png" alt=""></span><span>分类</span></li>
        </ul>
         <div class="container">
             <div class="example" @click="Tofirst()">
                 <img src="@/assets/img/云铺/资源 96.png" alt="">
                 <div class="explain">
                    <span class="mention">爆款</span>
                    <span class="title">2022 苗族土家族湘西舞蹈服装苗家舞台装</span>
                 </div>
                 <div class="condition">
                     <span class="left"><font-awesome-icon icon="fa-solid fa-yen-sign" /><span class="money"> 300.00</span></span>
                    <span class="pay">2000+人付款</span>
                 </div>
             </div>
             <div class="example" @click="Tosecond">
                 <img src="@/assets/img/云铺/资源 97.png" alt="">
                 <div class="explain">
                    <span class="mention">新品</span>
                    <span class="title">花边辅料领口袖口服装饰品配件苗族风布料条</span>
                 </div>
                 <div class="condition">
                     <span class="left"><font-awesome-icon icon="fa-solid fa-yen-sign" /><span class="money"> 20.10</span></span>
                    <span class="pay">100+人付款</span>
                 </div>
             </div>
             <div class="example" @click="Tothird">
                 <img src="@/assets/img/云铺/资源 98.png" alt="">
                 <div class="explain">
                    <span class="mention">爆款</span>
                    <span class="title">2022 苗族土家族湘西舞蹈服装苗家舞台装</span>
                 </div>
                 <div class="condition">
                     <span class="left"><font-awesome-icon icon="fa-solid fa-yen-sign" /><span class="money"> 300.00</span></span>
                    <span class="pay">2000+人付款</span>
                 </div>
             </div>
             <div class="example" @click="Toforth">
                 <img src="@/assets/img/云铺/资源 99.png" alt="">
                 <div class="explain">
                    <span class="mention">爆款</span>
                    <span class="title">2022 苗族土家族湘西舞蹈服装苗家舞台装</span>
                 </div>
                 <div class="condition">
                     <span class="left"><font-awesome-icon icon="fa-solid fa-yen-sign" /><span class="money"> 3.00</span></span>
                    <span class="pay">10+人付款</span>
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
        Tofirst(){
            this.$router.push('/shopFirst')
        },
        Tosecond(){
             this.$router.push('/village')
        },
        Tothird(){
             this.$router.push('/village')
        },
        Toforth(){
             this.$router.push('/village')
        },
        routerToshopCart(){
             this.$router.push('/shopCart')
        }
    }
}
</script>

<style scoped lang="scss">
.top{
    display: flex;
    align-items: center;
    height: 80px;
    .position{
        position: relative;
        margin-top: 15px;
        display: flex;
        width: 400px;
        align-items: center;
        input{
            height: 55px;
            border: none;
            outline: none;
            width: 450px;
            background-color:rgb(247, 245, 241) ;
            border-radius: 30px;
            padding-left: 70px;
            box-sizing: border-box;
            font-size: 16PX;
            margin-left: 20px;
        }
        .glass{
            position:absolute;
            left: 40px;
        }
        .camera{
            position: absolute;
            right: 10px;
        }
    }
    .icon{
        margin-top: 10px;
        margin-left: auto;
        margin-right: 60px;
        img{
            margin-left: 60px;
        }
    }
}
.rank{
    display: flex;
    justify-content: space-around;
    height: 150px;
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
            background-color: rgb(239, 213, 213) !important;
            margin-bottom: 5px;
        }
        img{
            width: 70px;
            height: 70px;
        }
    }
}
.container{
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    .example{
        background-color: rgb(250, 241, 241);
        width: 350px;
        height: 440px;
        display: flex;
        flex-wrap: wrap;
        border-radius: 15px;
        justify-content: center;
        margin-top: 20px;
        img{
            width: 300px;
            margin-top: 5px;
        }
        .explain{
            margin: 0 15px;
            font-size: 15PX;
            .mention{
                color: white;
                background-color: rgb(235, 101, 101);
                padding: 0 5px 0 5px;
                width:60px;
                border-radius: 15px;
                margin-right: 5px;
            }
            .title{
                font-weight: lighter;
            }
        }
        .condition{
            font-size: 15PX;
            color:rgb(235, 101, 101);
            width: 100%;
            display: flex;
            align-items: center;
            .left{
                margin-left: 30px;
                .money{
                    color:rgb(235, 101, 101); ;
                    font-size: 25PX;
                }
            }
            .pay{
                font-size: 13px;
                color: grey;
                margin-left: auto;
                margin-top: 10px;
                margin-right: 10px;
            }
        }
    }
}
</style>

<style scoped>
::v-deep .el-carousel__container,.el-carousel__item{
    display: flex;
    align-items: center;
    justify-content: center;
}
::v-deep .el-carousel__button
{
    margin-bottom: 38px;
    width: 60px;
    height: 5px;
    background-color: white !important;;
}
</style>
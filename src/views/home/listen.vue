<template>
    <div>
        <topNav></topNav>
        <el-carousel trigger="hover" height="150px" arrow="never">
            <el-carousel-item v-for="item in 4" :key="item">
                <img src="@/assets/img/听集/资源 20.png" alt="">
            </el-carousel-item>
        </el-carousel>
        <el-scrollbar wrapClass="scrollbar-wrap">
            <ul class="rank">
                <li class="getLeft"><span class="border"><img src="@/assets/img/听集/资源 21.png" alt=""></span><span>必听榜</span></li>
                <li><span class="border"><img src="@/assets/img/听集/资源 22.png" alt=""></span><span>推荐榜</span></li>
                <li><span class="border"><img src="@/assets/img/听集/资源 23.png" alt=""></span><span>排行榜</span></li>
                <li><span class="border"><img src="@/assets/img/听集/资源 24.png" alt=""></span><span>歌手榜</span></li>
                <li><span class="border"><img src="@/assets/img/听集/资源 46.png" alt=""></span><span>歌手榜</span></li>
            </ul>
        </el-scrollbar>
         <div class="announce">
            <font-awesome-icon icon="fa-solid fa-volume-high"  class="icon"/>
            <span class="msg">今日份的个人推荐歌单来啦！！！</span>
        </div>
        <div class="title">
            <span class="like">猜你喜欢</span>
            <span class="change"><font-awesome-icon icon="fa-solid fa-arrows-rotate" />换一批</span>
        </div>     
        <div>
            <div class="container" @click="routeToListen()">
                <img src="@/assets/img/听集/资源 25.png" alt="">
                <div class="name">
                    <span>沂蒙山小调(改编版)</span>
                    <span class="rank">超过50%播放</span>
                </div>
                <img src="@/assets/img/听集/资源 31.png" alt="" class="icon">
            </div>
             <div class="container">
                <img src="@/assets/img/听集/资源 27.png" alt="">
                <div class="name">
                    <span>贫女 <span class="author">-五三</span></span>
                </div>
                <img src="@/assets/img/听集/资源 31.png" alt="" class="icon">
            </div>
             <div class="container">
                <img src="@/assets/img/听集/资源 28.png" alt="">
                <div class="name">
                    <span>采莲曲 <span class="author">-邓丽君</span></span>
                </div>
                <img src="@/assets/img/听集/资源 31.png" alt="" class="icon">
            </div>
        </div>   
        <div class="title">
            <span class="like">歌单推荐</span>
            <span class="change"><font-awesome-icon icon="fa-solid fa-arrows-rotate" />换一批</span>
        </div>  
    </div>
</template>

<script>
import topNav from '../../components/topNav.vue'

export default {
    data(){
        return{
           
        }
    },
    components:{
        topNav,
    },
    methods:{
        routeToListen(){
            this.$router.push('/listenDetail')
        },
    }
}
</script>

<style scoped lang="scss">
.rank{
    display: flex;
    height: 100px;
    .getLeft{
        margin-left: 50px;
    }
    li{
        width: 120px;
        height: 80px;
        font-size: 13PX;
        margin-left: 85px;
        display: flex;
        flex-wrap: wrap;
        align-items: center;
        justify-content: center;
        .border{
            border-radius: 50%;
            width: 100px;
            height:100px;
            display: flex;
            justify-content: center;
            align-items: center;
            background-color: rgb(239, 213, 213) !important;
            margin-bottom: 5px;
        }
        img{
            width: 65px;
            height: 65px;
        }
    }
}
.announce{
    width: 90%;
    margin: 0 50px;
    background-color: rgb(247, 245, 241);
    margin-top: 15PX;
    border-radius: 8PX;
    height: 50px;
    display: flex;
    align-items: center;
    .icon{
        margin-left: 50px;
    }
    .msg{
        margin-left: 25px;
        font-size: 13PX;
    }
}
.title{
    margin-top:40px; 
    display: flex;
    align-items: center;
    .like{
        font-size: 20PX;
        font-family: 'Courier New', Courier, monospace;
        font-weight: bold;
        margin-left: 30px;
    }
    .change{
        margin-left: auto;
        margin-right: 30px;
        color: gray;
        font-size: 13PX;
    }
}
.container{
    display: flex;
    margin: 0 30px;
    background-color:   rgb(247, 245, 241);
    border-radius: 20px;
    height: 150px;
    align-items: center;
    margin-top: 10px;
    img{
        margin-left: 20px;
        width:120px;
        height: 120px;
    }
    .name{
        font-weight: 600;
        margin-left: 30px;
        .rank{
            color:rgb(115, 117, 65);
            background-color: rgb(234, 231, 221);
            height: auto;
            width: 180px;
            display: flex;
            margin-left: -10px;
            justify-content: center;
        }
        .author{
            margin-left: 20px;
            color: grey;
            opacity: 0.7;
            font-weight: normal;
        }
    }
    .icon{
        width: 80px;
        height: 80px;
        margin-left: auto;
        margin-right: 30px;
        opacity: 0.6;
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
::v-deep .el-scrollbar{
    height: 140px;
}
::v-deep .el-scrollbar__wrap{
  overflow-x: auto;
  overflow-y: hidden;
  white-space: nowrap;
  padding-bottom: 10px;
}
</style>


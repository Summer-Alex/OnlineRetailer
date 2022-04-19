<template>
    <div>
        <topNav></topNav>
        <el-carousel trigger="hover" height="150px" arrow="never">
            <el-carousel-item v-for="item in 4" :key="item">
                <img src="@/assets/img/视集/资源 3.png" alt="">
            </el-carousel-item>
        </el-carousel>
        <ul class="rank">
            <li><span class="border"><img src="@/assets/img/视集/资源 18.png" alt=""></span><span>必看榜</span></li>
            <li><span class="border"><img src="@/assets/img/视集/资源 4.png" alt=""></span><span>推荐榜</span></li>
            <li><span class="border"><img src="@/assets/img/视集/资源 5.png" alt=""></span><span>排行榜</span></li>
            <li><span class="border"><img src="@/assets/img/视集/资源 6.png" alt=""></span><span>全部分类</span></li>
        </ul>
        <div class="announce">
            <font-awesome-icon icon="fa-solid fa-volume-high"  class="icon"/>
            <span class="msg">你期待的、新创作的民歌来啦！！！</span>
        </div>
            <div class="title">
                <span class="like">猜你喜欢</span>
                <span class="change"><font-awesome-icon icon="fa-solid fa-arrows-rotate" />换一批</span>
            </div>
            <el-scrollbar>
            <div class="example">
                <div class="container topLeft">
                    <img src="@/assets/img/视集/资源 7.png" alt="" class="top">
                    <span class="time">5:45</span>
                    <span class="name">江南小调-茉莉花</span>
                    <span class="rank">全站播放量TOP1</span>
                </div>
                <div class="container topRight" @click="routeToDetail()">
                    <img src="@/assets/img/视集/资源 9.png" alt="" class="big">
                    <span class="time">5:23</span>
                    <span class="name">山丹丹花开红艳艳</span>
                    <span class="rank">全站播放量TOP2</span>
                </div>
                <div class="container bottomLeft">
                    <img src="@/assets/img/视集/资源 10.png" alt="" class="small">
                    <span class="time">5:43</span>
                    <span class="name">桃花酒</span>
                    <span class="rank">全站播放量TOP3</span>
                </div>
                <div class="container bottomRight">
                    <img src="@/assets/img/视集/资源 11.png" alt="" class="big">
                    <span class="time">6:11</span>
                    <span class="name">沂蒙山小调</span>
                    <span class="rank">全站播放量TOP4</span>
                </div>
            </div>
            </el-scrollbar>
    </div>
</template>

<script>
import topNav from '@/components/topNav.vue'
export default {
    data(){
        return{

        }
    },
    methods:{
        routeToDetail(){
            this.$router.push('/songDetail')
        }
    },
    components:{
        topNav
    }
}
</script>

<style scoped lang="scss">
.rank{
    display: flex;
    justify-content: space-around;
    height: 100px;
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
            width: 60px;
            height: 60px;
        }
    }
}
.announce{
    width: 90%;
    margin: 0 50px;
    background-color: rgb(247, 245, 241);
    margin-top: 20PX;
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
    .like{
        font-size: 20PX;
        font-weight: bold;
        margin-left: 30px;
        font-family: 'Courier New', Courier, monospace;
    }
    .change{
        margin-left: auto;
        color: grey;
        margin-right: 30px;
        font-size: 13PX;
    }
}
.example{
    margin-top: 10px;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    margin-right: 20px;
    height: 620px;
    .topLeft{
        border-radius: 10px 0 0 0;
        border: 10px solid rgb(239, 213, 213);
        border-right: none;
    }
    .topRight{
        border-radius: 0 10px 0 0;
        border: 10px solid rgb(239, 213, 213);
    }
    .bottomLeft{
        border-radius: 0 0 0 10px ;
        border: 10px solid rgb(239, 213, 213);
        border-right: none;
        border-top: none;
    }
    .bottomRight{
        border-radius: 0 0 10px 0 ;
        border: 10px solid rgb(239, 213, 213);
        border-top: none;
    }
    .container{
        width: 330px;
        position: relative;
        img{
            width: 350px;
            height: 200px;
        }
        .time{
            position: absolute;
            right: 50px;
            bottom: 100px;
            width: 90px;
            display: flex;
            justify-content: center;
            font-size: 10px;
            color: white;
            background-color: rgb(222, 176, 176);
        }
        .name{
            margin-left: 30px;
        }
        .rank{
            color: rgb(226, 131, 123);
            border-radius: 5px;
            font-size: 8PX;
            border: 1px solid rgb(226, 131, 123);
            margin-left: 30px;
            height: auto;
            box-sizing: border-box;
            padding: none ;
            width: 200px;
        }
        .big{
            width: 290px;
            height: 200px;
            margin-left: 30px;
            margin-top: 10px;
        }
        .small{
            width: 400px;
            margin-top: 8px;
        }
        .top{
            height: 210px;
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
    margin-bottom: 30px;
    width: 60px;
    height: 5px;
    background-color: white !important;;
}
::v-deep .el-scrollbar{
    height: 600px;
}
</style>


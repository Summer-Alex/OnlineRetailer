<template>
    <div>
        <div id="background"></div>
        <div class="icon">
            <img src="@/assets/img/播放界面2/资源 31.png" alt=""  @click="routerBack()">
        </div>
        <div class="song">
            <img src="@/assets/img/播放界面2/song.png" alt="" class="back">
            <img src="@/assets/img/播放界面2/资源 24.png" alt="" class="name">
        </div>
        <div class="container">
            <div class="word">
                <span>我们俩划着船儿</span>
                <span>采红菱</span>
                <span>呀采红菱</span>
            </div>
            <div class="word isPlay">
                <span>得呀得郎有情</span>
                <span>得呀得妹有心</span>
            </div>
            <div class="word">
                <span>就好像两角菱</span>
                <span>也是同日生</span>
            </div>
        </div>
        <div class="songName">
            <span>采红菱</span>
            <img src="@/assets/img/播放界面1/资源 8.png" alt=""  class="like">
        </div>
        <div class="author">
            <span>邓丽君</span>
            <span class="vedio">视频</span>
                <div class="react">
                    <img src="@/assets/img/播放界面1/资源 15.png" alt="">
                    <img src="@/assets/img/播放界面1/资源 16.png" alt="">
                    <img src="@/assets/img/播放界面1/资源 17.png" alt="" class="small">
                </div>
        </div>
        <div class="bottom">
            <div class="time">
                    <el-slider v-model="value" :show-tooltip="false"></el-slider>
                    <span>01:01</span>
                    <span class="right">03:30</span>
            </div>
            <playNav></playNav>
        </div>
    </div>
</template>

<script>
import playNav from "@/components/play.vue"
export default {
    data(){
        return{
            value: 30
        }
    },
    methods:{
        routerBack(){
            this.$router.go(-1)
        }
    },
    components:{
        playNav
    },
}
</script>

<style scoped lang="scss">
.icon{
    margin-top: 30px;
    margin-left: 30px;
}
.song{
    margin: 0 auto;
    width: 550px;
    position: relative;
    .back{
        width: 550px;
        height: 550px;
    }
    .name{
        position:absolute;
        top: 50px;
        left: 120px;
    }
}
.container{
    width: 550px;
    margin: 0 auto;
    margin-top: 30px;
    .word{
        display: flex;
        justify-content: space-around;
        color: rgb(219, 206, 206);
        font-size: 28px;
        margin-top: 10px;
    }
    .isPlay{
        color: rgb(240, 168, 167);
        font-size: 38px;
    }
}
.songName{
    font-size: 50px;
    color: rgb(232, 100, 95);
    display: flex;
    align-items: center;
    margin: 20px 40px 0 40px;
}
.like{
    margin-left: auto;
}
.author{
    margin: 20px 40px 0 50px;
    display: flex;
    align-items: center;
    color: rgb(214, 214, 214);
    font-size: 30px;
    .vedio{
        background-color: rgb(196, 192, 192);
        color: black;
        opacity: 0.7;
        margin-left: 15px;
        font-size: 24px;
        padding: 2px 8px;
        border-radius: 10px;
    }
    .react{
        margin-left: auto;
        img{
            margin-right: 50px;
        }
        .small{
            margin-bottom: 18px;
        }
    }
}
.bottom{
    width: 650px;
    margin: 0 auto;
.time{
    color: rgb(169, 165, 165);
    font-weight: lighter;
    font-size: 25px;
    margin-top: 30px;
    margin-bottom: 60px;
    .right{
        float: right;
    }
}
}
</style>

<style scoped>
#background{
opacity:1;
background: linear-gradient(white,rgb(57,48,45));
background-size: cover;
width:100%;
height:100%;
position:fixed;
z-index: -99;
}
::v-deep .el-slider__bar{
    background-color: rgb(249, 172, 172);
}
</style>
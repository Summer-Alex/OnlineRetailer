<template>
    <div class="positon:relative"  @click="cancle($event);cancleTimer()">
        <div id="background"></div>
        <div><img src="@/assets/img/播放界面1/资源 31.png" alt="" class="icon" @click="routeBack()"></div>
        <div class="bottom" v-show="ifDialog">
            <div class="song">
                <span>采红菱</span>
                <img src="@/assets/img/播放界面1/资源 8.png" alt=""  class="like">
            </div>
            <span class="name">邓丽君</span>
            <h2 class="word">词:我们俩划着船儿</h2>
            <div class="click">
                <button @click="showDialog()">查看剧情</button>
                <div class="icon">
                    <img src="@/assets/img/播放界面1/资源 15.png" alt="">
                    <img src="@/assets/img/播放界面1/资源 16.png" alt="">
                    <img src="@/assets/img/播放界面1/资源 17.png" alt="" class="small">
                </div>
            </div>
            <div class="time">
                 <el-slider v-model="value" :show-tooltip="false"></el-slider>
                 <span>01:01</span>
                 <span class="right">03:30</span>
            </div>
            <playNav></playNav>
        </div>
        <div class="dialog" ref="contentWrapper"> 
            <my-dialog 
        :title="title"
		:showDialog="isShowDialog"
		@closeDialog="isShowDialog=false"></my-dialog>
        </div>
    </div>
</template>

<script>
import MyDialog from "@/components/dialog.vue"
import playNav from "@/components/play.vue"
export default {
    data(){
        return{
            value:30,
            isShowDialog:false,
            count:0,
            ifDialog:true,
            title:'剧情介绍',
            timer:'',
            time:0
        }   
    },
    methods:{
        routeBack(){
            this.$router.push('/watch')
        },
        showDialog(){
        this.isShowDialog=true
        this.count=1
        this.ifDialog=false
    },
    cancle(e){
        let tree = this.$refs.contentWrapper.contains(e.target)
        if(!tree){
            this.count++
                if(this.count==3)
                {
                    this.isShowDialog=false
                    this.ifDialog=true
                }
            }
    },
    cancleTimer(){
        clearInterval(this.timer)
    }
    },
    components:{
        MyDialog,
        playNav
    },
    mounted(){
        this.timer=setInterval(() => {
            this.time++
            console.log(this.time)
            if (this.time==5)
            {
                this.$router.push('/vedio')
            }
        }, 1000);
    },
    beforeDestroy(){
        if (this.timer)
        {
            clearInterval(this.timer)
        }
    }
}
</script>


<style lang="scss" scoped >
.icon{
    margin-top: 30px;
    margin-left: 30px;
}
.bottom{
    margin-top: 716px;
    height: 600px;
    z-index: 99;
    width: 100%;
    box-sizing: border-box;
    padding-left: 60px;
    padding-right: 60px;
    background: linear-gradient(to bottom,rgba(255,255,255,0.1),rgba(38,29,28,1));
    .song{
        opacity: 1;
        font-size: 50px;
        color: rgb(232, 100, 95);
        display: flex;
        align-items: center;
    }
    .like{
        margin-left: auto;
    }
}
.name{
font-size: 30px;
margin-top: 10px;
display: inline-block;
color: rgb(241, 241, 241);
}
.word{
margin-top: 20px;
font-weight: lighter;
color: rgb(241, 241, 241) ;
}
.click{
    margin-top: 10px;
    display: flex;
    align-items: center;
    button{
        background: none;
        outline: none;
        border: none;
        color: rgb(241, 241, 241);
        width: 150px;
        text-align: left;
    }
    .icon{
        margin-left: auto;
        img{
            margin-right: 50px;
        }
        .small{
            margin-bottom: 18px;
        }
    }
}
.time{
    color: rgb(169, 165, 165);
    font-weight: lighter;
    font-size: 25px;
    .right{
        float: right;
    }
}
</style>



<style scoped>
#background{
opacity:1;
background: url('../../../assets/img/播放界面1/资源 7.png');
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
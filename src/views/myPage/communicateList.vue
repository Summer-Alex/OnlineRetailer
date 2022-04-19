<template>
    <div>
        <div class="top">
            <font-awesome-icon icon="fa-solid fa-arrow-left" @click="routeBack()"  class="icon"/>
            <span class="msg">X</span>
        </div>
        <span class="time">3月2日 12:00</span>
        <div class="X">
            <img src="@/assets/img/聊天页面/资源 19.png" alt="">
            <span class="msg">你好!</span>
        </div>
        <div class="X">
            <img src="@/assets/img/聊天页面/资源 19.png" alt="">
            <span class="msg">我很喜欢你发的动态</span>
        </div>
        <div class="my">
            <span class="msg">谢谢你的鼓励呀</span>
            <img src="@/assets/img/聊天页面/资源 18.png" alt="">
        </div>
        <div class="X">
            <img src="@/assets/img/聊天页面/资源 19.png" alt="">
            <span class="msg">你下次可以发一些关于小调的吗</span>
        </div>
        <div class="X">
            <img src="@/assets/img/聊天页面/资源 19.png" alt="">
            <span class="msg">我很喜欢这类</span>
        </div>
        <div class="my">
            <span class="msg">好的,没问题,我会多多考虑的</span>
            <img src="@/assets/img/聊天页面/资源 18.png" alt="">
        </div>
        <div class="X">
            <img src="@/assets/img/聊天页面/资源 19.png" alt="">
            <span class="msg">我还想转载你的视频和歌曲</span>
        </div>
        <div class="X">
            <img src="@/assets/img/聊天页面/资源 19.png" alt="">
            <span class="msg">我像更多人看见</span>
        </div>
        <div class="my">
            <span class="msg"> OK!,但是不要商用哦</span>
            <img src="@/assets/img/聊天页面/资源 18.png" alt="">
        </div>
        <div class="X">
            <img src="@/assets/img/聊天页面/资源 19.png" alt="">
            <span class="msg">谢谢你!</span>
        </div>
        <div class="click">
            <img src="@/assets/img/聊天页面/资源 15.png" alt="" class="left">
            <input type="text">
            <img src="@/assets/img/聊天页面/资源 16.png" alt="">
            <img src="@/assets/img/聊天页面/资源 17.png" alt="">            
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
            this.$router.push('/communicate')
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
.time{
    display: flex;
    color: grey;
    justify-content: center;
    margin-top: 15px;
}
.X{
    display: flex;
    align-items: center;
    padding-left: 50px;
    margin-top: 20px;
    .msg{
        background-color: rgb(239, 213, 213);
        display: flex;
        align-items: center;
        height: 60px;
        margin-left: 20px;
        padding-left: 20px;
        justify-content: center;
        padding-right: 30px;
        font-size: 28px;
        border-radius: 15px;
    }
}
.my{
    display: flex;
    align-items: center;
    justify-content: flex-end;
    padding-right: 50px;
    margin-top: 20px;
    .msg{
        background-color: rgb(236, 129,129);
        display: flex;
        align-items: center;
        height: 60px;
        margin-right: 20px;
        padding-left: 20px;
        justify-content: center;
        padding-right: 30px;
        font-size: 28px;
        border-radius: 15px;
    }
}
.click{
    display: flex;
    justify-content: center;
    margin-top: 100px;
    input{
        background-color: rgb(226, 226, 226);
        outline: none;
        border: none;
        width: 500px;
        border-radius: 15px;
    }
    img{
        margin-left: 20px;
    }
    .left{
        margin-right: 20px;
    }
}
</style>
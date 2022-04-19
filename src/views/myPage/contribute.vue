<template>
    <div>
        <img src="@/assets/img/投稿/资源 25.png" alt="" @click="routerBack()" class="icon">
        <div class="container">
            <h1>山歌与我</h1>
            <span class="msg">草长莺飞二月天,一起感受自然与山歌</span>
            <div class="position">
                <img src="@/assets/img/投稿/资源 1.png" alt="">
                <button class="click">点击参与</button>
            </div>
        </div>
        <div class="container">
            <h1>民歌之美</h1>
            <span class="msg">民歌征集活动正在进行中ing,奖励丰厚哦</span>
            <div class="position">
                <img src="@/assets/img/投稿/资源 2.png" alt="">
                <button class="click">点击参与</button>
            </div>
        </div>
        <div class="update">
            <div class="put">
                <img src="@/assets/img/投稿/资源 3.png" alt="">
                <img src="@/assets/img/投稿/资源 5.png" alt="" class="back">
                <span class="msg">上传视频</span>
            </div>
            <div class="put">
                <img src="@/assets/img/投稿/资源 4.png" alt="">
                <img src="@/assets/img/投稿/资源 6.png" alt="" class="back">
                <span class="msg">上传视频</span>
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
        routerBack(){
            this.$router.push('/myPage')
        },
    },
}
</script>



<style scoped lang="scss">
.icon{
    margin-top: 30px;
    margin-left: 50px;
}
.container{
    margin-left: 50px;
    margin-top: 20px;
    .msg{
        margin-top: 15px;
        display: inline-block;
        color: rgb(235, 101, 101);
    }
    .position{
        position: relative;
        display: flex;
        width: 650px;
        justify-content: center;
        img{
            width: 600px;
        }
        .click{
            position: absolute;
            bottom: 60px;
            right: 60px;
            outline: none;
            border: none;
            background-color: white;
            width: 130px;
            height: 60px;
            border-radius: 20px;
        }
    }
}
.update{
    display: flex;
    justify-content: space-around;
    margin-left: 50px;
    margin-right: 50px;
    margin-top: 20px;
    .put{
        background-color: rgb(235, 101, 101);
        display: flex;
        justify-content: center;
        align-items: center;
        width: 280px;
        height: 180px;
        border-radius: 20px;
        color: rgb(241, 241, 241);
        position: relative;
        font-size: 30px;
    }
    .back{
        position: absolute;
        right: 0;
        bottom: 0;
        opacity: 0.6;
    }
}
</style>
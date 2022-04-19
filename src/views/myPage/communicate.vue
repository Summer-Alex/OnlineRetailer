<template>
    <div>
        <div class="top">
            <font-awesome-icon icon="fa-solid fa-arrow-left" @click="routeBack()"  class="icon"/>
            <span class="msg">消息</span>
        </div>
        <input type="text" placeholder="搜索" class="search">
        <div class="container">
            <div class="example">
                <img src="@/assets/img/联系人/资源 12.png" alt="" class="green">
                <span class="msg">@我的</span>
            </div>
            <div class="example">
                <img src="@/assets/img/联系人/资源 13.png" alt="" class="blue">
                <span class="msg">评论</span>
            </div>
            <div class="example">
                <img src="@/assets/img/联系人/资源 14.png" alt="" class="yellow">
                <span class="msg">赞</span>
            </div>
            <div class="example">
                <img src="@/assets/img/联系人/资源 18.png" alt="">
                <div class="msg">
                    <span>123木</span>
                    <br>
                    <span class="title">hello</span>
                </div>
                <span class="mention">1</span>
            </div>
            <div class="example" @click="routerToCommunicateList()">
                <img src="@/assets/img/联系人/资源 19.png" alt="">
                <div class="msg">
                    <span>X</span>
                    <br>
                    <span class="title">谢谢你!</span>
                </div>
            </div>
            <div class="example">
                <img src="@/assets/img/联系人/资源 20.png" alt="">
                <div class="msg">
                    <span>月月</span>
                    <br>
                    <span class="title">我们支持你!!!</span>
                </div>
            </div>
            <div class="example">
                <img src="@/assets/img/联系人/资源 21.png" alt="">
                <div class="msg">
                    <span>两月</span>
                    <br>
                    <span class="title">哇哦,原来如此!</span>
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
        routeBack(){
            this.$router.push('/myPage')
        },
        routerToCommunicateList(){
            this.$router.push('/communicateList')
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
    .icon{
        position: absolute;
        left: 20px;
    }
}
.search{
    width: 90%;
    margin-left: 40px;
    margin-right: 40px;
    border: none;
    outline: none;
    background-color: rgb(224, 224, 224);
    height: 50px;
    border-radius: 15px;
    padding-left: 50px;
    box-sizing: border-box;
    margin-top: 30px;
    
}
::placeholder{
    color: rgb(119, 119, 119);
    padding-left: 45%;
    font-size: 27px;
}
.container{
    padding-left: 30px;
    padding-right: 30px;
    margin-top: 30px;
    .example
    {
        height: 150px;
        display: flex;
        align-items: center;
        border-bottom: 1px solid grey ;
        img{
            width: 100px;
            height: 100px;
        }
        .green{
            width: 60px;
            padding: 20px;
            height: 60px;
            border-radius: 50%;
            background-color: #9ED4C6;
        }
        .blue{
            width: 60px;
            padding: 20px;
            height: 60px;
            border-radius: 50%;
            background-color: #A6C5DC;
        }
        .yellow{
            width: 60px;
            padding: 20px;
            height: 60px;
            border-radius: 50%;
            background-color: #EDE9CC;
        }
        .msg{
            font-size: 28px;
            margin-left: 30px;
            .title{
                color: grey;
                font-size: 24px;
            }
        }
        .mention{
            margin-left: auto;
            margin-right: 50px;
            color: white;
            width: 50px;
            height: 50px;
            background-color: rgb(235, 101, 101);
            border-radius: 50%;
            display: flex;
            font-size: 30px;
            justify-content: center;
            align-items: center;
            font-weight: lighter;
        }
    }
}
</style>
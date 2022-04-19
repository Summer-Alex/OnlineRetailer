<template>
    <div>
        <div class="top">
            <span class="msg">消息</span>
        </div>
        <input type="text" placeholder="搜索" class="search">
        <div class="container">
            <div class="example">
                <div class="back">
                    <img src="@/assets/img/消息/资源 14.png" alt="" class="offical">
                </div>
                <div class="msg">
                    <span>笑看民歌官方</span>
                    <br>
                    <span class="title">最新通知如下:</span>
                </div>
            </div>
            <div class="example">
                <img src="@/assets/img/消息/资源 15.png" alt="">
                <div class="msg">
                    <span>123木</span>
                    <br>
                    <span class="title">你好,快递发什么快递</span>
                </div>
                <span class="mention">1</span>
            </div>
            <div class="example">
                <img src="@/assets/img/消息/资源 16.png" alt="">
                <div class="msg">
                    <span>X</span>
                    <br>
                    <span class="title">谢谢你!</span>
                </div>
            </div>
            <div class="example">
                <img src="@/assets/img/消息/资源 17.png" alt="">
                <div class="msg">
                    <span>月月</span>
                    <br>
                    <span class="title">我想申请退款</span>
                </div>
            </div>
             <div class="example">
                <img src="@/assets/img/消息/资源 18.png" alt="">
                <div class="msg">
                    <span>两月</span>
                    <br>
                    <span class="title">帮助到您,是我们的荣幸,亲。</span>
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
        .back{
            display: flex;
            justify-content: center;
            align-items: center;
            width: 100px;
            height: 100px;
            background-color: rgb(247, 193, 193);
            border-radius: 50%;
            .offical{
                width: 60px;
                height: 60px;
            }
        }
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
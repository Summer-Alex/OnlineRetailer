<template>
    <div>
        <div class="top">
            <font-awesome-icon icon="fa-solid fa-arrow-left" @click="routerBack()"  class="icon"/>
            <span class="msg">详情</span>
        </div>   
        <div class="user">
            <div class="introduce">
                <img src="@/assets/img/详情/资源 22.png" alt="">
                <ul>
                    <li><span class="name">哆啦A梦</span></li>
                    <li><span class="sign weight"> 向你分享了一个视频</span></li>
                </ul>
            </div>
            <div class="vedio">
                    <img src="@/assets/img/详情/资源 25.png" alt="" class="top">
                    <span class="time">5:45</span>
                    <span class="name">江南小调-茉莉花</span>
            </div>    
            <ul class="show">
                <li><img src="@/assets/img/详情/资源 27.png" alt=""></li>
                <li><img src="@/assets/img/详情/资源 28.png" alt="" class="small"></li>
                <li><img src="@/assets/img/详情/资源 29.png" alt=""></li>
            </ul>     
        </div>
        <span class="like">
            <img src="@/assets/img/详情/资源 55.png" alt="">
            <span class="msg">月月、阿拉丁、乐多、X等22人觉得很赞</span>
        </span>
        <div class="container">
            <div class="example">
                <img src="@/assets/img/详情/资源 18.png" alt="">
                <div class="msg">
                    <span>123木</span>
                    <br>
                    <span class="title">我觉得也好好看</span>
                </div>
                <div class="mention">
                    <img src="@/assets/img/详情/资源 26.png" alt="">
                    <span class="msg">4</span>
                </div>
            </div>
            <div class="example">
                <img src="@/assets/img/详情/资源 19.png" alt="">
                <div class="msg">
                    <span>X</span>
                    <br>
                    <span class="title">特别喜欢这类</span>
                </div>
                <div class="mention">
                    <img src="@/assets/img/详情/资源 27.png" alt="">
                </div>
            </div>
            <div class="example">
                <img src="@/assets/img/详情/资源 20.png" alt="">
                <div class="msg">
                    <span>月月</span>
                    <br>
                    <span class="title">我也想要</span>
                </div>
                <div class="mention">
                    <img src="@/assets/img/详情/资源 27.png" alt="">
                </div>
            </div>   
            <div class="example">
                <img src="@/assets/img/详情/资源 21.png" alt="">
                <div class="msg">
                    <span>两月</span>
                    <br>
                    <span class="title">滴!民歌人卡!</span>
                </div>
                <div class="mention">
                    <img src="@/assets/img/详情/资源 27.png" alt="">
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
        routerBack(){
            this.$router.push('/village')
        },
    },
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
.user{
    padding-top: 25px;
    margin: 0 30px;
    .show{
        display: flex;
        justify-content: flex-end;
        margin-right: 50px;
        margin-top: 20px;
        li{
            margin-left: 20px;
        }
    }
 .vedio{
        width: 330px;
        position: relative;
        height: 250px;
        background-color:   rgb(247, 245, 241);
        margin-left: 170px;
        .top{
            width:330px;
            height: 250px;
        }
        .time{
            position: absolute;
            right: 10px;
            bottom: 10px;
            width: 90px;
            display: flex;
            justify-content: center;
            font-size: 10px;
            color: white;
            background-color: rgb(222, 176, 176);
        }
        .name{
            margin-left: 30px;
            margin-top: 10px;
            display: inline-block;
        }
    }
    .introduce{
        display: flex;
        margin: 0 20px 10px 20px;
        .add{
            height: 50px;
            border-radius: 25px;
            border: 2px solid rgb(222, 99, 97);
            color:rgb(222, 99, 97);
            background-color: white;
            margin-left: 140px;
            cursor: pointer;
            margin-top: 30px;
        }
        img{
            height: 120px;
            width: 120px;
        }
        ul{
            margin: 10px 0 0 30px;
            li{
                margin-top: 10px;
                .name{
                    font-size: 19PX;
                    font-weight: 600;
                }
                .sign{
                    letter-spacing: 2px;
                    margin-top: 10px;
                } 
                .weight{
                    font-weight: 600;
                }
            }          
        }
    }
}
.like{
    margin-left: 80px;
    margin-top: 10px;
    display: flex;
    align-items: center;
    .msg{
        margin-left: 20px;
        font-size: 25px;
    }
}
.container{
    margin-top: 20px;
     .example
    {
        padding-left: 50px;
        height: 150px;
        display: flex;
        align-items: center;
        border-bottom: 1px solid grey ;
        margin-left: 30px;
        margin-right: 30px;
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
            display: flex;
            align-items: center;
            font-weight: lighter;
            img{
                width: 50px;
                height: 50px;
            }
            .msg{
                font-size: 25px;
                margin-left: 5px;
            }
        }
    }
}
</style>

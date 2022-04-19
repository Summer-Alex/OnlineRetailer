<template>
    <div>
        <villageNav></villageNav>
        <ul class="rank">
            <li><span><img src="@/assets/img/云村/资源 40.png" alt=""></span><span>添加好友</span></li>
            <li><span><img src="@/assets/img/云村/资源 41.png" alt=""></span><span>云村好友</span></li>
            <li><span><img src="@/assets/img/云村/资源 42.png" alt=""></span><span>喵喵</span></li>
            <li><span><img src="@/assets/img/云村/资源 43.png" alt=""></span><span>月亮不是两月</span></li>
        </ul>
        <div class="user">
            <div class="introduce">
                <img src="@/assets/img/云村/资源 52.png" alt="">
                <ul>
                    <li><span class="name">洛洛子</span></li>
                    <li><span class="care">你的关注</span></li>
                    <li><span class="sign">云村的朋友们，你们好哇，初来乍到，这是我新作的民歌，希望大家能够喜欢！</span></li>
                </ul>
            </div>
            <div class="container">
                    <img src="@/assets/img/听集/资源 25.png" alt="">
                    <ul class="name">
                        <li>沂蒙山小调(改编版)</li>
                        <li class="author">-洛洛子</li>
                    </ul>
                    <img src="@/assets/img/听集/资源 31.png" alt="" class="icon">
            </div>       
            <div class="comment">
                <div class="toFlex">
                    <img src="@/assets/img/云村/资源 69.png" alt="" class="icon">
                    <span class="msg">123木:我来浅浅翻唱一段</span>
                </div>
                <img src="@/assets/img/云村/资源 59.png" alt="" class="voice">
                <div class="like">
                    <img src="@/assets/img/云村/资源 55.png" alt="">
                    <span class="msg">热评</span>
                </div>
            </div>
            <ul class="show">
                <li><img src="@/assets/img/云村/资源 57.png" alt=""> 2022</li>
                <li><img src="@/assets/img/云村/资源 56.png" alt="" class="small">540</li>
                <li><img src="@/assets/img/云村/资源 58.png" alt="">666</li>
            </ul>     
        </div>
        <div class="user bottom" @click="routerTovillageDetail()">
            <div class="introduce">
                <img src="@/assets/img/云村/资源 60.png" alt="">
                <ul>
                    <li><span class="name">哆啦A梦</span></li>
                    <li><span class="font">根据你的喜好推荐</span></li>
                    <li><span class="sign weight"> 向你分享了一个视频</span></li>
                </ul>
                <button class="add">
                    +关注
                </button>
            </div>
            <div class="vedio">
                    <img src="@/assets/img/视集/资源 7.png" alt="" class="top">
                    <span class="time">5:45</span>
                    <span class="name">江南小调-茉莉花</span>
            </div>    
            <ul class="show">
                <li><img src="@/assets/img/云村/资源 57.png" alt=""> 22</li>
                <li><img src="@/assets/img/云村/资源 56.png" alt="" class="small">4</li>
                <li><img src="@/assets/img/云村/资源 58.png" alt="">2</li>
            </ul>     
        </div>
    </div>
</template>

<script>
import villageNav from '@/components/villageNav.vue'
export default {
    data(){
        return{

        }
    },
    components:{
        villageNav
    },
    methods:{
        routerTovillageDetail(){
            this.$router.push('/villageDetail')
        }
    }
}
</script>

<style scoped lang="scss">
.rank{
    display: flex;
    height: 170px;
    margin: 20px 10px 0;
    li{
        width: 165px;
        height: 50px;
        font-size: 13PX;
        margin-left: 5px;
        font-weight: 500;
        display: flex;
        flex-wrap: wrap;
        align-items: center;
        justify-content: center;
        img{
            width: 120px;
            height: 120px;
        }
    }
}
.bottom{
    border-bottom: rgb(149, 145, 100) 5px solid;
}
.user{
    padding-top: 25px;
    margin: 0 30px;
    border-top: rgb(149, 145, 100) 5px solid;
 .vedio{
        width: 330px;
        position: relative;
        height: 250px;
        background-color:   rgb(247, 245, 241);
        margin-left: 170px;
        .top{
            width:330px;
            height: 200px;
        }
        .time{
            position: absolute;
            right: 40px;
            bottom: 50px;
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
                .care{
                    color: rgb(222, 99,97);
                    border: 2px solid rgb(222, 99, 97);
                    padding: 0 7px;
                    opacity: 0.8;
                    border-radius: 10px;
                }
                .font{
                    opacity: 0.5;
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
    .container{
        display: flex;
        background-color:   rgb(247, 245, 241);
        border-radius: 20px;
        height: 150px;
        align-items: center;
        margin-top: 10px;
        font-family: 'Courier New', Courier, monospace;
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
                box-sizing: border-box;
                padding-top: 10px;
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
    .comment{
        border-left: 2px solid black;
        margin-top: 25px;
        padding-left: 20px;
        position: relative;
        .toFlex{
                display:flex;
                align-items: center;        
            .icon{
                width: 35px;
                height: 35px;
                margin-right: 10px;
            }
            .msg{
                font-size: 0.02rem;
                letter-spacing: 2px;
            }
        }
        .voice{
            margin-left: 130px;
            margin-top: 10px;
        }
        .like{
            position: absolute;
            right: 30px;
            bottom: 20px;
            font-size: 18PX;
            color: rgb(222, 99, 97);
            font-weight: 600;
            display: flex;
            align-items: center;
            .msg{
                margin-bottom: -5px;
            }
        }
    }
    .show{
        display: flex;
        justify-content: space-around;
        margin-top: 15px;
        margin-bottom: 10px;
        li{
            display: flex;
            align-items: center;
            .small{
                height: 35px;
            }
            img{
                margin-right: 10px;
            }
        }
    }
}
</style>
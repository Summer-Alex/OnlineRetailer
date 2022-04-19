<template>
    <div>
        <div id="background"></div>
        <villageNav></villageNav>
        <roomButton></roomButton>
         <div class="link">
            <router-link to="/song" exact-active-class="get">全部</router-link>
            <router-link to="/new" exact-active-class="get">最新</router-link>
            <router-link to="/hot" exact-active-class="get">热门</router-link>
            <router-link to="/listenRoom" exact-active-class="get">听歌房</router-link>
            <router-link to="/singRoom" exact-active-class="get">唱歌房</router-link>
        </div>
        <div class="container">
            <div class="color2">
                <span class="title">听歌房</span>
                <h3 class="msg">听我想听</h3>
                <ul>
                    <li><img src="@/assets/img/歌房/资源 40.png" alt=""></li>
                    <li><img src="@/assets/img/歌房/资源 40.png" alt=""></li>
                    <li><img src="@/assets/img/歌房/资源 40.png" alt=""></li>
                    <li><img src="@/assets/img/歌房/资源 40.png" alt=""></li>
                    <li><img src="@/assets/img/歌房/资源 43.png" alt=""></li>
                    <li class="number">20人</li>
                </ul>
            </div>
             <div class="color4">
                <span class="title">听歌房</span>
                <h3 class="msg">山歌荟萃</h3>
                <ul>
                    <li><img src="@/assets/img/歌房/资源 40.png" alt=""></li>
                    <li><img src="@/assets/img/歌房/资源 40.png" alt=""></li>
                    <li class="number">2人</li>
                </ul>
            </div>
            <div class="color3">
                <span class="title">听歌房</span>
                <h3 class="msg">向经典致敬</h3>
                <ul>
                    <li><img src="@/assets/img/歌房/资源 41.png" alt=""></li>
                    <li class="number">1人</li>
                </ul>
            </div>
            <div class="color1">
                <span class="title">听歌房</span>
                <h3 class="msg">无标题</h3>
                <ul>
                    <li><img src="@/assets/img/歌房/资源 52.png" alt=""></li>
                    <li><img src="@/assets/img/歌房/资源 40.png" alt=""></li>
                    <li><img src="@/assets/img/歌房/资源 40.png" alt=""></li>
                    <li><img src="@/assets/img/歌房/资源 42.png" alt=""></li>
                    <li><img src="@/assets/img/歌房/资源 40.png" alt=""></li>
                    <li class="number">5人</li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script>
import villageNav from '@/components/villageNav.vue'
import roomButton from '@/components/roomButton.vue'
export default {
    data(){
        return{

        }
    },
     components:{
        villageNav,
        roomButton
    }
}
</script>

<style scoped lang="scss">
.link{
        align-items: center;
        display: flex;
        justify-content: space-around;
        font-size: 15PX;
        color: black;
        margin: 0 20px 0 20px;
        border-bottom: rgb(149, 145, 100) 5px solid;
        padding-bottom: 10px;
        .get{
            color: white;
            background-color: rgb(235, 101, 101);
            padding: 0 15px 0 15px;
            display: flex;
            align-items: center;
            border-radius: 15px;
        }
}
.container{
    margin-top:20px;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    height: 850px;
    .color1{
      background: linear-gradient(to right,#ED8180,#F0D5D5);
      color: white;
      font-size: 15PX;
      width: 300px;
      height: 250px;
      border-radius: 15px;
      margin-top: 30px;
    }
        .color2{
      background: linear-gradient(to right,#9ED4C6 ,#D1EBEF);
      color: white;
      font-size: 15PX;
      width: 300px;
      height: 250px;
      border-radius: 15px;
      margin-top: 30px;
    }
        .color3{
      background: linear-gradient(to right,#F4A986 ,#F1D3C7);
      color: white;
      font-size: 15PX;
      width: 300px;
      height: 250px;
      border-radius: 15px;
      margin-top: 30px;
    }
        .color4{
      background: linear-gradient(to right,#A6C5DC,#DDECF9);
      color: white;
      font-size: 15PX;
      width: 300px;
      height: 250px;
      border-radius: 15px;
      margin-top: 30px;
    }
        .color5{
      background: linear-gradient(to right,#C18EBE,#F1CDE1);
      color: white;
      font-size: 15PX;
      width: 300px;
      height: 250px;
      border-radius: 15px;
      margin-top: 30px;
    }
}
</style>

<style scoped>
#background{
opacity:1;
background: url('../../../assets/img/歌房/资源 35.png') right;
background-size: cover;
width:100%;
height:100%;
position:fixed;
z-index: -99;
}
.title{
          font-family:'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
          margin-left: 40px;
          margin-top: 30px;
          display: inline-block;
      }
      .msg{
          margin-top: 30px;
          margin-left: 40px;
          font-weight: 500;
          font-size: 20PX;
      }
      ul{
          display: flex;
          margin-top: 40px;
          margin-left: 50px;
          position: relative;
      }
                li{
              margin-left: -15px;
          }
          .number{
            position: absolute;
            right: 40px;
            color: rgb(243, 243, 243);
        }
          img{
                width: 40px;
                height: 40px
                }
</style>
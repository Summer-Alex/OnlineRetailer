<template>
    <div>
        <div class="container">
        <div class="link">
            <router-link to="/village" :class="{'get':isVillage}">云村</router-link>
            <router-link to="/song" :class="{'get':isSong}">歌房</router-link>
        </div>
        <div class="position">
            <img src="@/assets/img/云村/资源 49.png" alt="">
            <input type="text" placeholder="输入关键字"> 
        </div>
        </div>
    </div>
</template>

<script>
export default {
    data(){
        return{
            isVillage:false,
            isSong:false
        }
    },
  watch: {
    $route: {
      immediate: true, // 一旦监听到路由的变化立即执行
      handler(route) {
        if (route.path=='/village')
        {
            this.isVillage=true
        }
        else{
            this.isVillage=false
        }
        if (route.path=='/song'||route.path=='/hot'||route.path=='/new'||route.path=='/singRoom'||route.path=='/listenRoom')
        {
            this.isSong=true
        }
        else
        {
            this.isSong=false
        }
      },
    },
  }
}
</script>

<style scoped lang="scss">
.container{
    display: flex;
    height: 80px;
    align-items: center;
    .link{
        height: 60px;
        align-items: center;
        display: flex;
        width: 300px;
        justify-content: space-around;
        font-size: 18PX;
        color: grey;
        margin-left: 20px;
        .get{
            color: black;
            border-bottom: 2px solid black;
        }
    }
.position{
    position: relative;
    margin-top: 15px;
    display: flex;
    align-items: center;
    input{
        height: 55px;
        border: none;
        outline: none;
        width: 350px;
        background-color:rgb(247, 245, 241) ;
        border-radius: 30px;
        padding-left: 70px;
        box-sizing: border-box;
        font-size: 16PX;
        margin-left: 20px;
    }
    img{
        position:absolute;
        left: 30px;
    }
}
}
</style>
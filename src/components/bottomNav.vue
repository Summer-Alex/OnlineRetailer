<template>
  <div>
    <ul :style="{display:isShopCart}">
      <router-link to="/watch"><li :style="{'color':colorChange1}"><img :src="icon1" alt=""> 集</li></router-link>
      <router-link to="/village"><li :style="{'color':colorChange2}"><img :src="icon2" alt=""> 村</li></router-link>
      <li @click="pagePlay()"><el-button><img src="@/assets/img/视集/资源 17.png" alt="" class="icon"></el-button></li>
      <router-link to="/shop"><li :style="{'color':colorChange3}"><img :src="icon3" alt=""> 铺</li></router-link>
      <router-link to="/myPage"><li :style="{'color':colorChange4}">
       <img :src="icon4" alt="">
        <span>吾</span>
      </li></router-link>
    </ul>
  </div>
</template>

<script>
import house from '@/assets/img/歌房/资源 36.png'
import me from '@/assets/img/视集/资源 16.png'
import user from '@/assets/img/视集/资源 13.png'
import shop from '@/assets/img/视集/资源 14.png'
import houseRed from '@/assets/img/视集/资源 12.png'
import meRed from '@/assets/img/吾/资源 85.png'
import userRed from '@/assets/img/云村/资源 63.png'
import shopRed from '@/assets/img/云铺/资源 103.png'
export default {
  data(){
    return{
      colorChange1:'grey',
      colorChange2:'grey',
      colorChange3:'grey',
      colorChange4:'grey',
      icon1:house,
      icon2:user,
      icon3:shop,
      icon4:me,
      isShopCart:'flex',
      page:''
    }
  },
  components:{
  },
  methods:{
    pagePlay()
    {
      if(this.page=='/watch')
      {
        console.log(this.page)
        this.$router.push('/songDetail')
      }
    }
  },
watch:{
  $route:{
    handler(route)
    {
      let routePath=route.path
      this.page=routePath
      if(routePath=='/watch' ||routePath=='/listen')
      {
        this.icon1=houseRed
        this.colorChange1='black'
      }
      else{
        this.icon1=house
        this.colorChange1='grey'
      }
      if(routePath=='/village'||routePath=='/song'||routePath=='/singRoom'||routePath=='/new'||routePath=='/hot'||routePath=='/listenRoom'){
        this.icon2=userRed
        this.colorChange2='black'
      }
      else{
        this.icon2=user
        this.colorChange2='grey'
      }
      if(routePath=='/shop')
      {
        this.icon3=shopRed
        this.colorChange3='black'
      }
      else{
        this.icon3=shop
        this.colorChange3='grey'
      }
      if(routePath=='/myPage')
      {
        this.icon4=meRed
        this.colorChange4='black'
      }
      else{
        this.icon4=me
        this.colorChange4='grey'
      }
      if (routePath=='/'||routePath=='/shopFirst'||routePath=='/songDetail'||routePath=='/listenDetail' || routePath=='/vedio'||routePath=='/load'||routePath=='/identity'|| routePath=='/normalRegister'||routePath=='/shopRegister'||routePath=='/shopCart'||routePath=='/coin'||routePath=='/shopImformation'||routePath=='/communicate'||routePath=='/communicateList'||routePath=='/villageDetail'||routePath=="/businessMain"||routePath=="/businessCart"||routePath=="/businessInformation")
      {
        this.isShopCart='none'
      }
      else{
        this.isShopCart='flex'
      }
    }
  }
}
}
</script>

<style lang="scss" scoped>
ul{
  height: 100px;
  background-color: rgb(247, 245, 241);
  align-items: center;
  justify-content: space-around;
  margin-top: 30px;
  position: absolute;
  left: 0;
  right: 0;
  li{
    width: 40px;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;
    font-size: 30px;/*px*/
    .el-button{
      border: none;
      outline: none;
      padding: 0;
      background-color: rgb(247, 245, 241);
        .icon{
              width: 90px;
              height: 90px;
        }
    }
    img{
      padding-top: 10px;
      width: 60px;
      padding-bottom: 5px;
    }
    .border{
      height: 40px;
      padding: 10px 10px;
      color: rgb(235, 101, 101);
      background-color: rgb(239, 213, 213);
      border-radius: 50%;
      display: flex;
      position: relative;
    }
    .positon{
      position: absolute;
      top: 32%;
      font-size: 12px;
    }
  }
}
</style>


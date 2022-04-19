<template>
    <div>
    <ul>
      <router-link to="/businessMain"><li :style="{'color':colorChange1}"><img :src="icon1" alt=""> 集</li></router-link>
      <router-link to="/businessInformation"><li :style="{'color':colorChange2}"><img :src="icon2" alt=""> 村</li></router-link>
      <router-link to="/businessCart"><li :style="{'color':colorChange3}"><img :src="icon3" alt=""> 铺</li></router-link>
    </ul>
    </div>
</template>



<script>
// import house from '@/assets/img/主界面/资源 36.png'
// import houseRed from '@/assets/img/主界面/资源 8.png'
export default {
    data(){
        return{

        }
    },
    methods:{

    },
    // components:{
    //     house,
    //     houseRed
    // }
}
</script>


<style scoped lang="scss">

</style>



<style scoped>

</style>
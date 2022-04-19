<template>
    <div>
        <div id="background"></div>
        <div class="top" @click="routerBack()">
            <img src="@/assets/img/登录界面3/资源 15.png" alt="">
            <span class="title">注册</span>
        </div>
        <div class="choice">
            <span class="title">选择你的身份</span>
        </div>
        <div class="click">
                <button @click="routerToNormal()">普通用户</button>
                <button @click="routerToShop()">商家</button>
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
        routerBack()
        {
            this.$router.go(-1)
        },
        routerToNormal(){
            this.$router.push('/normalRegister')
        },
        routerToShop(){
            this.$router.push('/shopRegister')
        }
    },
    components:{

    }
}
</script>


<style scoped lang="scss">
.top{
    padding-top: 40px;
    padding-left: 40px;
    display: flex;
    color: grey;
    .title{
        font-size: 35px;
        margin-left: 10px;
        margin-top: 5px;
    }
}
.choice{
    width: 250px;
    margin: 0 auto;
    margin-top: 300px;
    .title{
        font-size: 40px;
    }
}
.click{
    width: 500px;
    margin: 0 auto;
    margin-top: 70px;
    button{
        height: 80px;
        width: 500px;
        background-color: white;
        border-radius: 15px;
        outline: none;
        border: none;
        font-size: 35px;
        margin-top: 80px;
    }
}
</style>

<style scoped>
#background{
opacity:1;
background: url('../../assets/img/登录界面1/资源 4.png') right;
background-size: cover;
width:100%;
height:100%;
position:fixed;
z-index: -99;
}
</style>

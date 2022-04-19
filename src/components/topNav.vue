<template>
    <div>
        <div class="topNav">
            <span class="msg">乐集</span>
            <div class="position">
                <img src="@/assets/img/云村/资源 49.png" alt="">
                <input type="text" placeholder="输入关键字"> 
            </div>
            <font-awesome-icon icon="fa-solid fa-bars" class="icon" />
        </div>
        <div class="link">
            <router-link to="/watch" exact-active-class="getRed">视</router-link>
            <router-link to="/listen" exact-active-class="getRed">听</router-link>
        </div>
    </div>
</template>

<script>
export default {
    data(){
        return{
            input:''
        }
    }
}
</script>

<style scoped lang="scss">
.topNav{
    display: flex;
    margin-top: 10px;
    height: 80px;
    align-items: center;
    justify-content: center;
    .position{
    position: relative;
    margin-top: 15px;
    display: flex;
    align-items: center;
    input{
        height: 55px;
        border: none;
        outline: none;
        width: 550px;
        background-color:rgb(247, 245, 241) ;
        border-radius: 30px;
        padding-left: 70px;
        box-sizing: border-box;
        font-size: 16PX;
        margin-left: 20px;
    }
    img{
        position:absolute;
        left: 40px;
    }
}
    .icon{
        display: flex;
        font-size: 30px;
        align-items: center;
        margin-left: 20px;
        margin-top: 20px;
    }
    .msg{
        font-size: 30px;/*px*/
        font-weight: bold;
        margin-right: 15px;
        margin-left: 5px;
        margin-top:10px;
    }
}
.link{
    height: 60px;
    align-items: center;
    display: flex;
    justify-content: space-around;
    font-size: 30px;/*px*/
    .getRed{
        color: rgb(235, 101, 101);
        border-bottom: 2px solid black;
    }
}
</style>
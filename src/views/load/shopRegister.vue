<template>
    <div>
        <div id="background"></div>
        <div class="top" @click="routerBack()">
            <img src="@/assets/img/登录界面4/资源 15.png" alt="">
            <span class="title">商家注册</span>
        </div> 
        <div class="container">
            <div class="positon">
                <input type="text" placeholder="输入手机号码">
                <img src="@/assets/img/登录界面4/资源 2.png" alt="">
            </div>
            <div class="positon">
                <input type="text" placeholder="输入昵称">
                <img src="@/assets/img/登录界面4/资源 9.png" alt="">
            </div>
            <div class="positon">
                <input type="text" placeholder="输入密码">
                <img src="@/assets/img/登录界面4/资源 13.png" alt="">
            </div>
            <div class="positon">
                <input type="text" placeholder="再次输入密码">
                <img src="@/assets/img/登录界面4/资源 13.png" alt="">
            </div>
            <div class="positon">
                <input type="text" placeholder="上传你的身份证">
                <img src="@/assets/img/登录界面4/资源 16.png" alt="">
            </div>
            <div class="photo">
                <button>正面</button>
                <button>国徽面</button>
            </div>
            <div class="positon">
                <input class="large" type="text" placeholder="上传你的营业执照和商标证">
                <img src="@/assets/img/登录界面4/资源 16.png" alt="">
            </div>
            <div class="photo">
                <button>营业执照</button>
                <button>商标证</button>
            </div>
            <div class="positon">
                <input type="text" placeholder="上传网银卡号">
                <img src="@/assets/img/登录界面4/资源 16.png" alt="">
            </div>
            <div class="positon">
                <input type="text" placeholder="输入验证码">
                <div class="get">
                    <button>获取验证码</button>
                </div>
            </div>
        </div>
        <div class="click">
            <button @click="enter()">注册</button>
        </div>
        <div class="agreement">
            <el-radio v-model="radio" label="2">您已阅读并同意《笑看民歌登录协议》</el-radio>
        </div>
    </div>
</template>


<script>
export default {
    data(){
        return{
            radio:''
        }
    },
    methods:{
        routerBack()
        {
            this.$router.go(-1)
        },
        enter(){
            this.$router.push('/businessMain')
        }
    },
    components:{

    }
}
</script>

<style scoped lang="scss">
.photo{
    margin-top: 40px;
    display: flex;
    justify-content: space-between;
    button{
        height: 130px;
        width: 45%;
        color: grey;
        font-size: 30px;
        outline: none;
        border: none;
    }
}
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
.container{
    width: 580px;
    margin: 0 auto;
    margin-top: 20px;
    .positon{
        position: relative;
        .large{
            padding-left: 150px;
        }
        input{
            width: 580px;
            height: 90px;
            border-radius: 15px;
            outline: none;
            border: none;
            margin-top: 50px;
            padding-left: 40%;
            box-sizing: border-box;
        }
        img{
            position: absolute;
            right: 30px;
            bottom:20px;
        }
        .get{
            position: absolute;
            right: 5px;
            bottom: 10px;
            button{
                width: 180px;
                height: 70px;
                border-radius: 45px;
                outline: none;
                border: none;
                font-size: 30px;
                background-color:rgb(235, 101, 101);
                color: white;
            }
        }
    }
}
.click{
    margin: 0 auto;
    width: 300px;
    margin-top: 60px;
    button{
        width: 270px;
        height: 80px;
        border-radius: 45px;
        outline: none;
        border: none;
        font-size: 30px;
        background-color:rgb(235, 101, 101);
        color: white;
    }
}
.agreement{
        margin-top: 80px;
        color: grey;
        font-size: 30px;
        display: flex;
        justify-content: center;
        height: 80px;
        input{
            border-radius: 20px;
        }
    }
</style>


<style scoped>
#background{
opacity:1;
background: url('../../assets/img/登录界面4/资源 4.png') right;
background-size: cover;
width:100%;
height:100%;
position:fixed;
z-index: -99;
}
::v-deep .el-radio__inner{
    width: 30px;
    height: 30px;
    border-radius: 10px;
    border: 3px solid rgb(232, 100, 95);
}
::v-deep .el-radio__label{
    font-size: 25px;
}
::v-deep .el-radio__input.is-checked+.el-radio__label{
    color: grey;
    border: none;

}
::v-deep .el-radio__input.is-checked .el-radio__inner{
background-color: rgb(232, 100, 95);;
border: none;
}
</style>
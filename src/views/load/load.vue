<template>
    <div>
        <div id="background"></div>
            <div class="user">
                <img src="@/assets/img/登录界面1/资源 7.png" alt="">
                <span>Your ID</span>
            </div>
            <div class="load">
                <div class="positon">
                    <input type="text" placeholder="输入账号">
                    <img src="@/assets/img/登录界面1/资源 2.png" alt="">
                </div>
                 <div class="positon">
                    <input type="text" placeholder="输入密码">
                    <img src="@/assets/img/登录界面1/资源 13.png" alt="">
                </div>
                <span class="forget">?忘记密码</span>
                <div class="agreement">
                      <el-radio v-model="radio" label="2">您已阅读并同意《笑看民歌登录协议》</el-radio>
                </div>
                <div class="click">
                    <button class="load" @click="enter()">登录</button>
                    <button class="register" @click="chooseIdentity()">注册</button>
                </div>
            </div>
            <div class="bottom">
                <img src="@/assets/img/登录界面1/资源 3.png" alt="">
                <img src="@/assets/img/登录界面1/资源 5.png" alt="">
                <img src="@/assets/img/登录界面1/资源 6.png" alt="">
            </div>
    </div>
</template>


<script>
export default {
    data(){
        return{
            radio:'',
        }
    },
    methods:{
        chooseIdentity(){
            this.$router.push('/identity')
        },
        enter(){
            this.$router.push('/watch')
        }
    },
    components:{
        
    },
}
</script>

<style scoped lang="scss">
.user{
    width: 200px;
    margin: 0 auto;
    padding-top: 180px;
    span{
        display: flex;
        justify-content: center;
        margin-right: 10px;
        color: white;
        font-size: 30px;
        font-weight: lighter;
    }
}
.load{
    width: 500px;
    margin: 0 auto;
    .positon{
        position: relative;
        input{
            width: 520px;
            height: 80px;
            border-radius: 15px;
            outline: none;
            border: none;
            margin-top: 50px;
            padding-left: 40%;
            box-sizing: border-box;
        }
        img{
            position: absolute;
            right: 0px;
            bottom:15px;
        }
    }
    .forget{
        display: flex;
        justify-content: flex-end;
        color: grey;
        margin-top: 10px;
        font-size: 25px;
    }
    .agreement{
        margin-top: 20px;
        color: grey;
        font-size: 25px;
        display: flex;
        justify-content: center;
        input{
            border-radius: 20px;
        }
    }
    .click{
        width: 270px;
        margin: 40px  auto;
        .load{
            width: 270px;
            height: 80px;
            border-radius: 45px;
            outline: none;
            border: none;
            font-size: 30px;
            background-color:rgb(235, 101, 101);
            color: white;
        }
        .register{
             width: 270px;
            height: 80px;
            border-radius: 45px;
            outline: none;
            border: none;
            font-size: 30px;
            color: grey;
            background-color: transparent;
        }
    }
}
.bottom
{
    display: flex;
    justify-content: space-around;
    margin-top: 150px;
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
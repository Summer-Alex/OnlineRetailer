<template>
    <div>
        <div id="background" @click="showInput"></div>
        <img src="@/assets/img/播放界面3/资源 33.png" alt="" class="icon" @click="routerBack">
        <transition name="s">
            <div class="float" v-if="word">
                <p><span>画风好赞,我好喜欢</span>
                <span>哇哦哦哦</span></p>
                <p><span>好甜好甜,awsl</span>
                <span>羡慕</span></p>
                <p><span>我也是</span>
                <span>阿珍爱上了阿强</span></p>
            </div>
        </transition>
        <div class="play">
            <img src="@/assets/img/播放界面3/资源 30.png" alt="" >
        </div>
        <transition name="s">
            <div class="word" v-if="input">
                <el-switch
                    v-model="value"
                    active-color="rgb(232, 100, 95)"
                    inactive-color="rgb(241, 241, 241)"
                    @change="showWord">
                </el-switch>    
                <div class="input">
                    <input type="text" placeholder="输入你的弹幕">
                    <img src="@/assets/img/播放界面3/资源 29.png" alt="" class="icon">
                </div>
            </div>
        </transition>
    </div>
</template>

<script>
export default {
    data(){
        return{
            value:'',
            word:true,
            input:true
        }
    },
    methods:{
        routerBack(){
            this.$router.push('/songDetail')
        },
        showWord(){
            console.log(this.value)
            if(this.value=="true")
            {
                this.word=true
                this.input=true
            }
            else
            {
                this.word=false
                this.input=false
            }
        },
        showInput(){
            this.input=true
            this.word=true
            this.value=true
        }
    },
    components:{
    }
}
</script>


<style lang="scss" scoped >
.icon{
    margin-top: 30px;
    margin-left: 30px;
}
.float{
    margin-top: 50px;
    font-size: 35px;
    p{
        color: rgb(232, 100, 95) !important;
        margin-left: 30px;
        display: flex;
        justify-content: space-around;
        margin-top: 30px;
    }
}
.play{
    position: fixed;
    top: 50%;
    left: 40%;
}
.word{
    position: fixed;
    bottom: 40px;
    display: flex;
    margin-left: 50px;
    align-items: center;
    .input{
        position: relative;
        input{
            width: 480px;
            height: 50px;
            border-radius: 20px;
            border: none;
            outline: none;
            padding-left: 40px;
            background-color: rgb(236, 219, 223);
            opacity: 0.9;
            margin-left: 50px;
        }
        .icon{
            position: absolute;
            right: 30px;
            bottom:5px;
        }
    }
}
</style>


<style scoped>
#background{
opacity:1;
background: url('../../../assets/img/播放界面3/资源 7.png');
background-size: cover;
width:100%;
height:100%;
position:fixed;
z-index: -99;
}
::v-deep  .el-switch__core{
height: 40px;
opacity: 0.8;
border-radius: 20px;
}
::v-deep  .el-switch__core::after{
    height: 44px;
    width: 40px;
    margin-top:-5px;
    margin-left: -20px;
}
.s-enter-active,
.s-leave-active {
  transition: all 0.5s;
}

.s-enter,.s-leave-to {
  opacity: 0;
}
</style>
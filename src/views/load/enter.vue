<template>
    <div>
            <div id="background"></div>
                <div class="icon">
                    <div class="back">
                        <img src="@/assets/img/加载/资源 11.png" alt="">
                    </div>
                    <img src="@/assets/img/加载/资源 10.png" alt="">
                </div>
    </div>
</template>

<script>
export default {
    data(){
        return{
            time:0,
            timer:''
        }
    },
    methods:{

    },
    components:{

    },
    mounted(){
        this.timer=setInterval(() => {
            this.time++
            console.log(this.time)
            if (this.time==3)
            {
                this.$router.push('/load')
            }
        }, 1000);
    },
    beforeDestroy(){
        clearInterval(this.timer)
    }
}
</script>

<style scoped lang="scss">
.icon{
    position: fixed;
    top: 30%;
    left: 30%;
    .back{
        display: flex;
        justify-content: center;
        align-items: center;
        width: 300px;
        height: 300px;
        background-color: rgb(247, 193, 193);
        border-radius: 50%;
        margin-bottom: 50px;
    }
}
</style>

<style scoped>
#background{
opacity:1;
background-color: rgb(239, 213, 213);
background-size: cover;
width:100%;
height:100%;
position:fixed;
z-index: -99;
}
.s-enter-active,
.s-leave-active {
  transition: all 0.5s;
}

.s-enter,.s-leave-to {
  opacity: 0;
}
</style>
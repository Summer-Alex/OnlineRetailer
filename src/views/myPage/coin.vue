<template>
    <div>
        <div class="top">
            <img src="@/assets/img/coin/资源 31.png" alt="" @click="routerBack()">
            <span class="msg" @click="discountShow()">详细说明</span>
        </div>
        <div class="left" @click="cancle($event)">
            <span class="result">余额</span>
            <div class="container">
                <div class="integral">
                    <div class="icon">
                        <img src="@/assets/img/coin/资源 34.png" alt="">
                        <input type="text" placeholder="请输入" v-model="integral">
                    </div>
                    <span class="title">乐师积分</span>
                </div>
                <button @click="change()">点击转换<font-awesome-icon icon="fa-solid fa-arrow-right-long"  /></button>
                <div class="integral">
                    <div class="icon">
                        <img src="@/assets/img/coin/资源 42.png" alt="">
                        <input type="text" placeholder="请输入" v-model="coin" disabled>
                    </div>
                    <span class="title">乐师币</span>
                </div>
            </div>
            <div class="mention">
                <img src="@/assets/img/coin/资源 36.png" alt="">
                <ul>
                    <li>100乐师积分 可转换为1乐师币</li>
                    <li>1乐师币 可转换为1人民币</li>
                </ul>
            </div>
            <ul class="important">
                <li>注意:1.人民币不可以转换为乐师币哦</li>
                <li class="put"><span class="red">2.云铺交易使用人民币</span>,不适用乐师币</li>
                <li class="put">3.乐师积分可兑换优惠卷,可在云铺消费时使用</li>
            </ul>
        </div>
        <div class="get" v-if="isDiscount">
            <span class="title">获取方式以及用途</span>
            <div class="msg">
                <span class="integral">乐师积分:</span>
                <ul>
                    <li>1.每日签到获得1积分</li>
                    <li>2.云铺消费每次获得2乐师积分</li>
                    <li>3.参与平台的“投稿”活动,投稿一次获得5积分</li>
                    <li>4.发布作品点击量安每1000个赞获得5乐师积分</li>
                </ul>
                <span class="red">乐师积分可用于兑换表情包、乐师币、优惠卷</span>
            </div>
             <div class="msg">
                <span class="integral">乐师币:</span>
                <ul>
                    <li>1.由100乐师积分兑换得到1乐师币</li>
                    <li>2.从“投稿”上传并被平台引用,平台对每首原创或改编民歌发放低价为500乐师币奖励</li>
                </ul>
                <span class="red">乐师积分可用于兑换人民币</span>
            </div>
        </div>
        <div ref="contentWrapper">
            <discount
            :title="title"
            :showDialog="isShowDialog"
            ></discount>
        </div>
    </div>
</template>


<script>
import discount from "@/components/discount.vue"
export default {
    data(){
        return{
            integral:'',
            coin:'',
            title:'test',
            isShowDialog:false,
            isDiscount:true,
            count:0,
        }
    },
    components:{
        discount
    },
    methods:{
        routerBack(){
            this.$router.push('/myPage')
        },
        change(){
            this.coin=this.integral/100
        },
        discountShow(){
            this.isShowDialog=true
            this.isDiscount=false
        },
        cancle(e){
            var temp=this.$refs.contentWrapper.contains(e.target)
            if(!temp){
            this.count++
                if(this.count==2)
                {
                    this.isShowDialog=false
                    this.isDiscount=true
                    this.count=0
                }
            }
        },
    }
}
</script>

<style scoped lang="scss">
.top{
    display: flex;
    margin-left: 30px;
    margin-right: 50px;
    margin-top: 30px;
    align-items: center;
    .msg{
        color: rgb(235, 101, 101);
        font-size: 30px;
        margin-left: auto;
    }
}
.left{
    margin-top: 40px;
    margin-left: 50px;
    margin-right: 50px;
    .result{
        font-size: 35px;
    }
    .container{
        display: flex;
        .integral{
            margin-top: 30px;
            width: 280px;
            border-radius: 15px;
            height: 200px;
            background-color: rgb(235, 101, 101);
            display: flex;
            flex-wrap: wrap;
            .icon{
                margin-left: 20px;
                margin-top: 30px;
                img{
                   width: 60px;
                   height: 60px;
                }
                    input{
                    outline: none;
                    border: none;
                    width: 150px;
                    height: 100px;
                    background-color: rgb(235, 101, 101);
                    margin-left: 30px;
                    color: white;
                    font-size: 40px;
                }
                ::-webkit-input-placeholder{
                    color: white;
                    font-size: 40px;
                }
            }
            .title{
                color: white;
                opacity: 0.6;
                font-size: 40px;
                width: 100%;
                display: flex;
                justify-content: flex-end;
                margin-right: 10px;
            }
        }
        button{
            outline: none;
            border: none;
            background-color: white;
            width: 130px;
            color: grey;
        }
    }
    .mention{
        display: flex;
        margin-top: 50px;
        font-size: 25px;
        ul{
            margin-left: 20px;
        }
    }
    .important{
        margin-top: 30px;
        margin-left: 10px;
        font-size: 27px;
        font-weight: lighter;
        .red{
            color:rgb(235, 101, 101) ;
        }
        .put{
            margin-left: 50px;
        }
    }
}
.get{
    opacity:1;
    background: url('../../assets/img/coin/资源 40.png') right bottom no-repeat;
    height: 670px;
    background-color: rgb(239, 213, 213);
    margin-left: 30px;
    margin-right: 30px;
    border-radius: 25px;
    margin-top: 40px;
    padding-left: 20px;
    .title{
        font-size: 40px;
        margin-top: 20px;
        display: inline-block;
    }
    .msg{
        margin-top: 30px;
        .integral{
            font-size: 35px;
        }
        ul{
            margin-top: 20px;
            margin-left: 10px;
            font-size: 25px;
            font-weight: lighter;
            li{
                margin-top: 5px;
            }
        }
        .red{
            color:rgb(235, 101, 101);
            font-size: 28px ;
            margin-top: 15px;
            display: inline-block;
            font-weight: 600;
        }
    }
}
</style>


<style scoped>

</style>
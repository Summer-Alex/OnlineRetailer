<template>
<div>
    <div class="room">
            <button class="link">
                <span class="title">创建房间</span>
                <span class="explain">点击创建欢乐房间</span>
            </button>
            <button class="link">
                <span class="title">进入房间</span>
                <span class="explain">输入邀请码进入</span>
            </button>
        </div>
</div>
</template>


<style scoped lang="scss">
.room{
    display: flex;
    height: 230px;
    align-items: center;
    justify-content: space-around;
    .link{
        width: 300px;
        height: 130px;
        border-radius: 20px;
        outline: none;
        border: none;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-wrap: wrap;
        background-color: rgb(239, 213, 213);
        .title{
            font-size: 25PX;
            font-weight: 700;
            letter-spacing: 5PX;
        }
        .explain{
            opacity: 0.5;
        }
    }
}
</style>

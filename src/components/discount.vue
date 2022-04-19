<template>
  <transition name="dialog">
    <div v-if="showDialog" id="dialog-bg" @touchmove.prevent @scroll.prevent>
      <div id="dialog">
        <el-scrollbar>
            <span class="title">优惠卷</span>
            <div class="container">
              <img src="@/assets/img/discount/discount3.png" alt="">
              <img src="@/assets/img/discount/discount1.png" alt="">
              <img src="@/assets/img/discount/discount2.png" alt="">
            </div>
        </el-scrollbar>
      </div>
    </div>
  </transition>
</template>

<script>
export default {
  props: {
    showDialog: Boolean,
    title:String,
  },

  methods: {
    close: function () {
      this.$emit("closeDialog");
    },
  },

  watch: {},
};
</script>


<style scoped lang="scss">
.title{
    font-size: 40px;
}
.container{
  width: 500px;
  margin: 0 auto;
  img{
    margin-top: 20px;
  }
}
</style>


<style>
* {
  box-sizing: border-box;
}

#dialog-bg {
  bottom: 0;
  left: 0;
  position: fixed;
  width: 100vw;
  height: 100px;
  z-index: 98;
}

#dialog {
  position: fixed;
  bottom: 0;
  width: calc(100% - 60px);
  margin-left: 50px;
  margin-right: 50px;
  height: 620px;
  background-color: white;
}

/* 适配电脑等大屏幕 */
@media (min-width: 750px) {
  #dialog {
    width: 500px;
    left: 0;
    right: 0;
    margin: 0 auto;
  }
}

.dialog-button {
  width: 100%;
  background-color: #6367d5;
  border-width: 0;
  border-radius: 360px;
  padding: 10px;
  outline: none;
  color: white;
}

.dialog-button:focus {
  outline: none;
}

.dialog-button:active {
  background-color: #585dbe;
  border-color: #585dbe;
}

.dialog-enter-active,
.dialog-leave-active {
  transition: all 0.5s;
}

.dialog-enter,
.dialog-leave-to {
  opacity: 0;
}
</style>
<style scoped>
::v-deep .el-scrollbar__view{
  background-color: white;
}
</style>>

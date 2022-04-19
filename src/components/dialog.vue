<template>
  <transition name="dialog">
    <div v-if="showDialog" id="dialog-bg" @touchmove.prevent @scroll.prevent>
      <div id="dialog">
        <div class="story">
            <span class="title">{{title}}</span>
            <ul>
                <li>哥哥与妹妹是家住对们的青梅竹马</li>
                <li>正巧碰上采红菱农忙时</li>
                <li>哥哥主动约着妹妹一路采红菱</li>
                <li>哥哥划着船</li>
                <li>妹妹玩弄着水</li>
                <li>这时突然发现了两角菱</li>
                <li>哥哥含蓄的说：这两角菱就像我和妹妹一般</li>
                <li>我在船尾划桨，你在船头摘红菱，像是一条心</li>
                <li>妹妹害羞的低下了头，红了脸，轻微的点点头</li>
            </ul>
        </div>
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

<style>
* {
  box-sizing: border-box;
}

#dialog-bg {
  top: 0;
  left: 0;
  position: fixed;
  width: 100vw;
  height: 100px;
  z-index: 98;
}

#dialog {
  border-radius: 20px 20px 0 0;
  position: fixed;
  bottom: 0;
  background: linear-gradient(to bottom,rgba(213,208,210,0.3),rgba(200,184,187,0.8));
  width: 100vw;
  padding: 15px;
  height: 500px;
  padding-bottom: 25px;
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

<style scoped lang="scss">
.story{
    color: rgb(241, 241, 241);
    margin-left: 50px;
    margin-top: 30px;
    .title{
        font-size: 40px;
        color: rgb(232, 100, 95);
    }
    ul{
        margin-top: 20px;
        li{
            font-size: 25px;
            margin-top: 5px;
        }
    }
}
</style>
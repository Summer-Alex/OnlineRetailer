<template>
  <div>
    <el-scrollbar>
      <router-view/>
      <!-- 360-420 650-731 -->
    </el-scrollbar>
    <bottomNav></bottomNav>
  </div>
</template>

<script>
import bottomNav from '@/components/bottomNav.vue';
export default {
  data(){
    return{
     
    }
  },
  components:{
    bottomNav
  },
}
</script>

<style scoped>
::v-deep .el-scrollbar{
height: 100%;
}
</style>


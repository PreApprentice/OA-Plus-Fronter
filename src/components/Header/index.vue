<template>
  <div class="header-box">
    <!-- Logo部分 -->
    <div
      style="display: flex; align-items: center; margin-left: 20px"
      @click="jumpHome('/login')"
    >
      <el-col :span="12">
        <div class="demo-basic--circle">
          <div class="block">
            <el-avatar
              shape="square"
              :size="35"
              :src="require('./fish.jpg')"
            ></el-avatar>
          </div>
        </div>
      </el-col>
    </div>
    <!-- 系统名称部分 -->
    <div
      style="
        display: flex;
        font-family: 微软雅黑;
        font-size: 20px;
        align-items: center;
        color: #ffffff;
        margin-left: 10px;
        font-weight: bolder;
      "
      @click="jumpHome('/register')"
    >
      华中大Vue学习系统
    </div>
    <!-- 右边部分 -->
    <div style="display: flex; align-items: center; margin-left: auto">
      <div style="margin-right: 25px">
        <el-badge :value="99" class="item" type="primary">
          <el-button @click="showMessage" size="small">消息</el-button>
        </el-badge>
      </div>
      <div style="margin-right: 10px">
        <el-col :span="12">
          <div class="demo-basic--circle">
            <div class="block">
              <el-avatar
                shape="square"
                :size="35"
                :src="require('./avatar.jpg')"
              ></el-avatar>
            </div>
          </div>
        </el-col>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "Header",

  methods: {
    jumpHome(name) {
      this.$router.push(name);
    },

    showMessage() {
      this.$notify.info({
        title: "消息",
        message: "您于2022年08月01日注册系统账户，欢迎使用！",
        offset: 50,
        showClose: false,
        duration: 3000,
      });
    },
  },
};
</script>
<style lang="css" scoped>
.header-box {
  display: flex;
  width: 100%;
  height: 8%;
  background-color: #245ff5;
}
</style>

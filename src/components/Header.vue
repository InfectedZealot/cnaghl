<template>
  <div>
    <el-menu
      background-color="#2e2e2e"
      text-color="#ffffff"
      active-text-color="#000000"
      class="el-menu-demo"
      mode="horizontal"
      @select="handleSelect"
      router
    >
      <el-menu-item index="/index"
        ><el-avatar
          :size="50"
          :src="require('../assets/images/header/lambda1.webp')"
        ></el-avatar
        >&nbsp;主页
      </el-menu-item>
      <el-menu-item index="/server">服务器</el-menu-item>
      <el-submenu index="/download" text-color="#ffffff">
        <template slot="title">下载</template>
        <el-menu-item index="/model">自定义模型</el-menu-item>
        <el-menu-item index="/sprite">自定义spr</el-menu-item>
        <el-menu-item index="/wadtexture">自定义纹理</el-menu-item>
        <!-- <el-submenu index="/client" text-color="#ffffff">
          <template slot="title">游戏客户端/补丁</template>
          <el-menu-item index="/client/BugfixedHL">BugfixedHL</el-menu-item>
          <el-menu-item index="/client/OpenAG">OpenAG</el-menu-item>
          <el-menu-item index="/client/AGMODX">AG MOD X</el-menu-item>
          <el-menu-item index="/client/TrainingMod">Training Mod</el-menu-item>
        </el-submenu> -->
        <el-menu-item index="/client">游戏客户端/补丁</el-menu-item>
      </el-submenu>
      <el-submenu index="/demovideo" text-color="#ffffff">
        <template slot="title">DEMO视频</template>
        <el-menu-item index="/matchvideo">比赛视频</el-menu-item>
        <el-menu-item index="/video">其他视频</el-menu-item>
      </el-submenu>
      <el-submenu index="/tutorial" text-color="#ffffff">
        <template slot="title">教程</template>
        <el-menu-item index="/commands">游戏指令说明</el-menu-item>
        <el-menu-item index="/weapon">武器使用</el-menu-item>
        <el-menu-item index="/basicskill">基础技巧</el-menu-item>
        <el-menu-item index="/advancedskill">进阶技巧</el-menu-item>
      </el-submenu>
      <el-menu-item index="/tournament">赛事</el-menu-item>
    </el-menu>
  </div>
</template>
<script>
export default {
  data() {
    return {};
  },
  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath);
    },
  },
};
</script>

<style>
.el-menu {
  border: 0 !important;
}


.el-submenu__title:hover,
.el-menu-item:focus,
.el-menu-item:hover {
  background-color: #ffa500 !important;
  color: white !important;
  box-shadow:2px 2px 10px !important;
}

.el-menu .el-menu-item.is-active{
  background-color: #ffa500 !important;
  color: white !important;
  border-bottom-color: #ffa500 !important;
}

.el-submenu .el-submenu__title {
  color: white !important;
}

.router-link-active {
  text-decoration: none;
}

a {
  text-decoration: none;
}
</style>
<template>
  <el-container>
    <el-aside>
      <aside-component />
    </el-aside>
    <el-container>
      <el-header>
        <el-menu class="el-menu-demo" mode="horizontal">
          <el-menu-item index="1">Processing Center</el-menu-item>
          <el-submenu index="2">
            <template slot="title">Workspace</template>
            <el-menu-item index="2-1">item one</el-menu-item>
            <el-menu-item index="2-2">item two</el-menu-item>
            <el-menu-item index="2-3">item three</el-menu-item>
          </el-submenu>
          <el-menu-item index="3" disabled>Info</el-menu-item>
          <el-menu-item index="4"><a href="https://www.ele.me" target="_blank">Orders</a></el-menu-item>
        </el-menu>
      </el-header>
      <el-main>
        <router-view/>
      </el-main>
    </el-container>
  </el-container>
</template>

<script>
import AsideComponent from '@/components/aside';
export default {
  components: {
    AsideComponent
  }
}
</script>
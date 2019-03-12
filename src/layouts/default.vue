<template>
  <el-container style="background: #f0f2f5;">
    <el-menu
      :collapse="collapse"
      class="aside-menu"
      :default-active="$route.path"
      router
      background-color="#001529"
      text-color="hsla(0,0%,100%,.67)"
    >
      <div class="logo">
        <nuxt-link to="/">
          <img class="logo-img" :src="$store.state.meta.logo" alt="logo" />
          <h1 class="logo-text">{{ $store.state.meta.appName }}</h1>
        </nuxt-link>
      </div>
      <menu-item :menuList="menuList"></menu-item>
    </el-menu>

    <el-container>
      <el-header>
        <el-row type
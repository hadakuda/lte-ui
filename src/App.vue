<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <Layout>
    <Header>
      <Menu mode="horizontal" theme="dark" active-name="1">
        <div class="layout-logo"></div>
        <div class="layout-nav">
          <MenuItem name="1">
          <Icon type="ios-navigate"></Icon>
          Item 1
          </MenuItem>
          <MenuItem name="2">
          <Icon type="ios-keypad"></Icon>
          Item 2
          </MenuItem>
          <MenuItem name="3">
          <Icon type="ios-analytics"></Icon>
          Item 3
          </MenuItem>
          <MenuItem name="4">
          <Icon type="ios-paper"></Icon>
          Item 4
          </MenuItem>
        </div>
      </Menu>
    </Header>
    <Layout>
      <Sider hide-trigger :style="{ background: '#fff' }">
        <Menu active-name="1-2" theme="light" width="auto" :open-names="['1']">
          <Submenu name="1">
            <template #title>
              <Icon type="ios-navigate"></Icon>
              Item 1
            </template>
            <MenuItem name="1-1">Option 1</MenuItem>
            <MenuItem name="1-2">Option 2</MenuItem>
            <MenuItem name="1-3">Option 3</MenuItem>
          </Submenu>
          <Submenu name="2">
            <template #title>
              <Icon type="ios-keypad"></Icon>
              Item 2
            </template>
            <MenuItem name="2-1">Option 1</MenuItem>
            <MenuItem name="2-2">Option 2</MenuItem>
          </Submenu>
          <Submenu name="3">
            <template #title>
              <Icon type="ios-analytics"></Icon>
              Item 3
            </template>
            <MenuItem name="3-1">Option 1</MenuItem>
            <MenuItem name="3-2">Option 2</MenuItem>
          </Submenu>
        </Menu>
      </Sider>
      <Layout :style="{ padding: '0 24px 24px' }">
        <Breadcrumb :style="{ margin: '24px 0' }">
          <BreadcrumbItem>Home</BreadcrumbItem>
          <BreadcrumbItem>Components</BreadcrumbItem>
          <BreadcrumbItem>Layout</BreadcrumbItem>
        </Breadcrumb>
        <Content :style="{ padding: '24px', minHeight: '280px', background: '#fff' }">
          <RouterView />
        </Content>
      </Layout>
    </Layout>
  </Layout>
</template>

<style scoped></style>

<script setup>
import ParentLayout from '@vuepress/theme-default/layouts/Layout.vue'
import ExtraSideBar from './ExtraSideBar.vue';
</script>

<template>
  <ParentLayout>
    <template #page-bottom>
      <div class="my-footer">This is my custom page footer</div>
    </template>
    <template #sidebar-top>
      <ExtraSideBar/>
    </template>
  </ParentLayout>
</template>

<style lang="css">
.my-footer {
  text-align: center;
}
</style>
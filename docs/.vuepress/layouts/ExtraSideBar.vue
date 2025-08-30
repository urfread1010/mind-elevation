<script setup>
import { ElButton } from 'element-plus'
import 'element-plus/dist/index.css'

const items = [
  { desc: '公众号', icon: '/images/wexin4.png', content: '/images/official_account.jpg' },
  {},
  {}, {}, {}
]
</script>

<template>
  <nav class="right-floating-nav">
    <div v-for="(item, index) in items" :key="index" class="nav-item">
      <!-- 有 icon 的按钮 -->
       <div v-if="item.icon">
        <el-button  type="primary" class="nav-btn">
          <img :src="item.icon" class="icon-img" />
        </el-button>
        <!-- 描述文字 -->
        <p class="nav-desc">{{ item.desc }}</p>
       </div>
      
      <!-- 空按钮 -->
      <el-button v-else type="primary" class="nav-btn empty-btn"></el-button>

      <!-- 悬停显示 content -->
      <img v-if="item.content" :src="item.content" class="hover-img" />
    </div>
  </nav>
</template>

<style scoped>
.right-floating-nav {
  position: fixed;
  top: 50%;
  right: 10px;
  transform: translateY(-50%);
  display: flex;
  flex-direction: column;
  gap: 1rem;
  z-index: 9999;
}

.nav-item {
  position: relative;
}

.nav-desc {
  font-size: 12px;
  color: #333;
  text-align: center;
  margin: 0;
}

.nav-btn {
  width: 50px;
  height: 50px;
  padding: 0;
  background-color: #ffffff;
  color: white;
  border: none;        /* 去掉边框 */
}

.empty-btn {
  background-color: #ffffff;
}

.icon-img {
  width: 24px;
  height: 24px;
}

.hover-img {
  display: none;
  position: absolute;
  top: 0;               /* 对齐按钮顶部 */
  left: -160px;         /* 按钮宽度 + margin */
  width: 150px;
  height: 150px;
  object-fit: contain;
  border: 1px solid #ccc;
  background: #fff;
  z-index: 10;
}

.nav-item:hover .hover-img {
  display: block;
  
}
.nav-btn:hover {
  background-color: #ccc;
}
</style>

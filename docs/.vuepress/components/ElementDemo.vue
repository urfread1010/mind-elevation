<template>
  <div>
    <el-button type="primary" @click="dialogVisible = true">
      点我弹窗
    </el-button>

    <el-dialog
      title="测试弹窗"
      v-model="dialogVisible"
      width="30%"
    >
      <p>这里是 Element Plus 弹窗内容！</p>
      <span slot="footer" class="dialog-footer">
        <el-button @click="dialogVisible = false">取 消</el-button>
        <el-button type="primary" @click="dialogVisible = false">确 定</el-button>
      </span>
    </el-dialog>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import 'element-plus/dist/index.css'

const dialogVisible = ref(false)
</script>

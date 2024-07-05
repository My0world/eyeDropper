<template>
  <div class="card" data-tauri-drag-region>
    <div class="content">
      <n-color-picker :value="sRGBHex" size="large" :show="false" />
      <el-button type="primary" size="small" @click="handleClick">
        点击拾取色
      </el-button>
    </div>
  </div>
</template>


<script setup>
import { useEyeDropper } from '@vueuse/core'
import { NColorPicker } from 'naive-ui'



const { open, sRGBHex } = useEyeDropper()

const handleClick = async () => {
  open()
}


</script>


<style lang="less">
body {
  margin: 0;

  .card {
    width: 100px;
    height: 80px;
    padding: 5px;
    box-sizing: border-box;
    border: 1px solid #fff;

    .content {
      width: 100%;
      height: 100%;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      align-items: center;
    }
  }
}
</style>


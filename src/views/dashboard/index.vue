<template>
  <section class="home-box">
    <div class="side-logo">
      <transition enter-active-class="animate__animated animate__fadeInLeft">
        <span class="logo-title">零信任信息化平台</span>
      </transition>
    </div>
  
    
    <div style="margin-top: 30px">
      <el-timeline style="max-width: 600px">
        <el-timeline-item
            v-for="(activity, index) in activities"
            :key="index"
            :icon="activity.icon"
            :type="activity.type"
            :color="activity.color"
            :size="activity.size"
            :hollow="activity.hollow"
            :timestamp="activity.timestamp"
        >
          {{ activity.content }}
        </el-timeline-item>
      </el-timeline>
    </div>
  </section>
</template>

<script setup>
import { MoreFilled } from '@element-plus/icons-vue'
import setting from '@/setting.js'
const activities = [
  {
    content: '完善细节',
    timestamp: '2024-09-05 00:00',
    type: 'primary',
  },
  {
    content: '基础布局完成',
    timestamp: '2024-08-28 14:30',
    type: 'primary',
    hollow: true,
  },
  {
    content: '项目初始化搭建',
    timestamp: '2024-07-15',
  },
]
</script>


<style lang="scss" scoped>
.home-box {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  .info-box {
    font-size: 15px;
    color: #6c6c6c;
    text-align: center;
    line-height: 1.8;
  }

}
.side-logo {
  height: $navbar-height;
  line-height: $navbar-height;
  font-weight: bold;
  font-size: 50px;
  font-family: "Courier New";
  color: var(--el-color-primary);
  margin: 15px;
}
</style>

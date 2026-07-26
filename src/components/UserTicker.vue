<template>
  <div class="glass-card ticker-card">
    <div class="ticker-wrapper">
      <div v-for="(item, index) in tickerItems" :key="index" class="ticker-item">
        <span>{{ item.text }}</span>
        <span style="color: var(--success-color); font-weight: bold;">[生成完成]</span>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const tickerItems = ref([
  {
    "text": "用户 137****3322 完成了深夜职场焦虑共情与正念呼吸引导"
  },
  {
    "text": "用户 189****5510 生成了失恋情感断联期的自爱与心理抚慰"
  },
  {
    "text": "用户 131****9900 完成了完美主义拖延愧疚感认知重塑"
  },
  {
    "text": "用户 156****4411 生成了面对 30 岁年龄焦虑的温和拥抱报告"
  },
  {
    "text": "用户 173****8890 取得了恢复能量的 3 个微小行动建议"
  }
]);
</script>

<script setup lang="ts">
import { withBase } from 'vitepress'
import AtlasVendors from './AtlasVendors.vue'
import UiIcon from './UiIcon.vue'
const heroTitle = '从架构演进，\n看到计算发生。'
</script>

<template>
  <section class="hg-atlas-page">
    <nav class="hg-atlas-breadcrumb" aria-label="当前位置">
      <a :href="withBase('/')"><UiIcon name="arrow" :size="16" />Hello GPU</a>
      <span>GPU ATLAS</span>
    </nav>
    <header class="hg-atlas-page-hero">
      <p class="hg-atlas-page-kicker">GPU ATLAS · GPU 图谱</p>
      <h1>{{ heroTitle }}</h1>
      <p>沿着 GPU 的每一层，连接整卡、芯片与计算单元。把教程中的抽象概念，放回看得见的硬件结构。</p>
    </header>
    <AtlasVendors />
    <div class="hg-atlas-reading-note"><UiIcon name="book" :size="22" /><p>图谱用于辅助理解硬件与查阅公开资料。架构模型是结构示意；产品规格、理论峰值与教程实测分别标注。</p><a :href="withBase('/curriculum/')">回到学习路线 <UiIcon name="arrow" :size="18" /></a></div>
  </section>
</template>

<style scoped>
.hg-atlas-page {
  max-width: 1456px;
  margin: auto;
  padding: 40px 48px 90px;
  color: var(--vp-c-text-1);
}

.hg-atlas-breadcrumb {
  display: flex;
  gap: 20px;
  align-items: center;
  font-size: 12px;
  color: var(--vp-c-text-3);
}

.hg-atlas-breadcrumb a {
  display: inline-flex;
  align-items: center;
  gap: 9px;
  color: var(--vp-c-text-2);
}

.hg-atlas-breadcrumb a svg {
  transform: rotate(180deg);
}

.hg-atlas-breadcrumb > span {
  padding-left: 20px;
  border-left: 1px solid var(--vp-c-divider);
  font-size: 10px;
  letter-spacing: .06em;
}

.hg-atlas-page-hero {
  padding: 76px 0 64px;
}

.hg-atlas-page-kicker {
  font: 11px var(--vp-font-family-mono);
  letter-spacing: .13em;
  color: var(--vp-c-text-3);
  margin: 0 0 26px;
}

.hg-atlas-page h1 {
  font-size: clamp(43px, 5.2vw, 72px);
  line-height: 1.2;
  letter-spacing: -.045em;
  font-weight: 600;
  white-space: pre-line;
  margin: 0;
}

.hg-atlas-page-hero > p:last-child {
  max-width: 620px;
  font-size: 18px;
  line-height: 1.9;
  color: var(--vp-c-text-2);
  margin: 28px 0 0;
}

.hg-atlas-reading-note {
  display: flex;
  align-items: center;
  gap: 20px;
  margin-top: 32px;
  color: var(--vp-c-text-3);
}

.hg-atlas-reading-note > svg {
  flex-shrink: 0;
}

.hg-atlas-reading-note p {
  margin: 0;
  font-size: 13px;
  line-height: 1.8;
  max-width: 720px;
}

.hg-atlas-reading-note a {
  margin-left: auto;
  color: var(--vp-c-brand-1);
  display: flex;
  align-items: center;
  gap: 12px;
  white-space: nowrap;
  font-size: 13px;
}

@media (max-width: 1000px) {
  .hg-atlas-page {
    padding: 32px 32px 70px;
  }
  .hg-atlas-reading-note {
    flex-wrap: wrap;
  }
  .hg-atlas-reading-note a {
    margin: 4px 0 0 42px;
  }
}

@media (max-width: 700px) {
  .hg-atlas-page {
    padding: 30px 24px 60px;
  }
  .hg-atlas-page-hero {
    padding: 55px 0 40px;
  }
  .hg-atlas-page h1 {
    font-size: clamp(37px, 9vw, 58px);
  }
  .hg-atlas-page-hero > p:last-child {
    font-size: 16px;
    margin-top: 24px;
  }
  .hg-atlas-page-kicker {
    font-size: 10px;
    margin-bottom: 22px;
  }
  .hg-atlas-reading-note {
    align-items: flex-start;
    gap: 15px;
  }
  .hg-atlas-reading-note p {
    flex: 1;
    min-width: 200px;
    font-size: 12px;
  }
  .hg-atlas-reading-note a {
    margin-left: 37px;
  }
}
</style>

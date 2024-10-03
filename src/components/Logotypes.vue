<script setup lang="ts">
import { onMounted, ref } from 'vue'

const logos = ref([
  'amazon.png',
  'dribbble.png',
  'hubspot.png',
  'notion.png',
  'netflix.png',
  'zoom.png'
])
</script>

<template>
  <div class="logotypes">
    <div class="three">
      <img src="/logos/amazon.png" alt="" />
      <img src="/logos/dribbble.png" alt="" />
      <img src="/logos/hubspot.png" alt="" />
      <img src="/logos/notion.png" alt="" />
      <img src="/logos/netflix.png" alt="" />
      <img src="/logos/zoom.png" alt="" />
    </div>
    <div class="three second-row">
      <img src="/logos/zoom.png" alt="" />
      <img src="/logos/netflix.png" alt="" />
      <img src="/logos/notion.png" alt="" />
      <img src="/logos/hubspot.png" alt="" />
      <img src="/logos/dribbble.png" alt="" />
      <img src="/logos/amazon.png" alt="" />
    </div>
  </div>
</template>

<style lang="scss">
@keyframes scroll {
  0% {
    transform: translateX(0%);
  }
  100% {
    transform: translateX(-50%);
  }
}

@keyframes scroll-reverse {
  0% {
    transform: translateX(0%);
  }
  100% {
    transform: translateX(50%);
  }
}

.logotypes {
  width: 100%;
  overflow: hidden;
  display: flex;
  gap: 20px 95.8px;

  .three {
    display: flex;
    gap: 95.8px;
  }

  img {
    zoom: 0.5;
  }
}

@media only screen and (max-width: 1280px) {
  .logotypes {
    flex-direction: column;

    .three {
      animation: scroll 10s linear infinite;
    }

    .second-row {
      flex-direction: row-reverse;
      animation: scroll-reverse 10s linear infinite;
    }
  }
}
@media only screen and (max-width: 800px) {
  .logotypes {
    flex-direction: column;
  }
}
</style>

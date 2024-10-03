<script setup lang="ts">
import OneService from '@/components/OneService.vue'
</script>

<template>
  <div class="all-services">
    <OneService
      background-title="green"
      color="gray"
      title="Search engine optimization"
      image="services/first.png"
    />
    <OneService
      background-title="white"
      color="green"
      title="Pay-per-click advertising"
      image="services/second.png"
    />
    <OneService
      background-title="white"
      color="black"
      title="Social Media Marketing"
      image="services/third.png"
    />
    <OneService
      background-title="green"
      color="gray"
      title="Email Marketing"
      image="services/fourth.png"
    />
    <OneService
      background-title="white"
      color="green"
      title="Content Creation"
      image="services/fifth.png"
    />
    <OneService
      background-title="green"
      color="black"
      title="Analytics and Tracking"
      image="services/third.png"
    />
  </div>
</template>

<style lang="scss">
.all-services {
  margin-top: 80px;
  display: flex;
  gap: 40px;
  flex-wrap: wrap;
}

@media only screen and (max-width: 800px) {
  .all-services {
    margin-top: 40px;
    gap: 40px 0px;
  }
}
</style>

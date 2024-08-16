<script setup lang="ts">
import WorkingProcess from '@/components/WorkingProcess.vue'

const data = [
  {
    title: 'Consultation',
    text: 'During the initial consultation, we will discuss your business goals and objectives, target audience, and current marketing efforts. This will allow us to understand your needs and tailor our services to best fit your requirements.'
  },
  {
    title: 'Research and Strategy Development',
    text: 'unknown'
  },
  {
    title: 'Implementation',
    text: 'unknown'
  },
  {
    title: 'Monitoring and Optimization',
    text: 'unknown'
  },
  {
    title: 'Reporting and Communication',
    text: 'unknown'
  },
  {
    title: 'Continual Improvement',
    text: 'unknown'
  }
]
</script>

<template>
  <div class="all-working">
    <WorkingProcess
      v-for="(one, index) in data"
      key="index"
      :id="index"
      :title="one.title"
      :text="one.text"
    />
  </div>
</template>

<style lang="scss">
.all-working {
  margin-top: 80px;
  display: flex;
  flex-direction: column;
  gap: 30px;
}
</style>

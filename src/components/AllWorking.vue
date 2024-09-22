<script setup lang="ts">
import WorkingProcess from '@/components/WorkingProcess.vue'

const data = [
  {
    title: 'Consultation',
    text: 'During the initial consultation, we will discuss your business goals and objectives, target audience, and current marketing efforts. This will allow us to understand your needs and tailor our services to best fit your requirements.'
  },
  {
    title: 'Research and Strategy Development',
    text: 'In this phase, we conduct thorough market research to understand the competitive landscape, customer behavior, and industry trends. Based on these insights, we develop a comprehensive marketing strategy tailored to your business goals.'
  },
  {
    title: 'Implementation',
    text: 'We execute the marketing strategy by launching campaigns across various channels, creating content, and engaging with your target audience. This phase involves coordinating all activities to ensure a cohesive approach.'
  },
  {
    title: 'Monitoring and Optimization',
    text: 'We continuously monitor the performance of marketing campaigns using analytics tools. Based on the data collected, we optimize the campaigns to improve their effectiveness and achieve better results.'
  },
  {
    title: 'Reporting and Communication',
    text: 'Regular reports are generated to keep you informed about the progress and performance of the marketing efforts. We maintain open communication to discuss results, insights, and any necessary adjustments.'
  },
  {
    title: 'Continual Improvement',
    text: 'We believe in continuous improvement. By analyzing past performance and gathering feedback, we make incremental changes to enhance the effectiveness of our marketing strategies and ensure sustained success.'
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

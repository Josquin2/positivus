<script setup lang="ts">
import Header from '@/components/Header.vue'
import FirstView from '@/components/FirstView.vue'
import Logotypes from '@/components/Logotypes.vue'
import Divider from '@/components/Divider.vue'
import AllServices from '@/components/AllServices.vue'
import Proposal from '@/components/Proposal.vue'
import AllWorking from '@/components/AllWorking.vue'
</script>

<template>
  <div class="positivus-main-page">
    <Header />
    <FirstView />
    <Logotypes />
    <Divider
      title="Services"
      text="At our digital marketing agency, we offer a range of services to help businesses grow and succeed online. These services include:"
      :max-width="580"
    />
    <AllServices />
    <Proposal />
    <Divider
      title="Case Studies"
      text="Explore Real-Life Examples of Our Proven Digital Marketing Success through Our Case Studies"
      :max-width="580"
    />
    <AllWorking />
  </div>
</template>

<style lang="scss"></style>

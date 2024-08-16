<script setup lang="ts">
import Header from '@/components/Header.vue'
import FirstView from '@/components/FirstView.vue'
import Logotypes from '@/components/Logotypes.vue'
import Divider from '@/components/Divider.vue'
import AllServices from '@/components/AllServices.vue'
import Proposal from '@/components/Proposal.vue'
import AllWorking from '@/components/AllWorking.vue'
import TeamMembers from '@/components/TeamMembers.vue'
import Testimonials from '@/components/Testimonials.vue'
import Contact from '@/components/Contact.vue'
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
    <Divider
      title="Team"
      text="Meet the skilled and experienced team behind our successful digital marketing strategies"
      :max-width="473"
    />
    <TeamMembers />
    <Divider
      title="Testimonials"
      text="Hear from Our Satisfied Clients: Read Our Testimonials to Learn More about Our Digital Marketing Services"
      :max-width="473"
    />
    <Testimonials />
    <Divider
      title="Contact Us"
      text="Connect with Us: Let's Discuss Your Digital Marketing Needs"
      :max-width="323"
    />
    <Contact />
    <footer class="footer">
      <div class="top"></div>
      <div class="middle"></div>
      <div class="divider"></div>
      <div class="bottom"></div>
    </footer>
  </div>
</template>

<style lang="scss">
.footer {
  margin: 140px 0px 0px 0px;
  padding: 55px 60px 50px 60px;
  background-color: #191a23;
  border-radius: 45px 45px 0px 0px;
}
</style>

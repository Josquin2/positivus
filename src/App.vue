<script setup lang="ts">
import Header from '@/components/Header.vue'
import FirstView from '@/components/FirstView.vue'
import Logotypes from '@/components/Logotypes.vue'
import Divider from '@/components/Divider.vue'
import AllServices from '@/components/AllServices.vue'
import Proposal from '@/components/Proposal.vue'
import CaseStudies from '@/components/CaseStudies.vue'
import AllWorking from '@/components/AllWorking.vue'
import TeamMembers from '@/components/TeamMembers.vue'
import Testimonials from '@/components/Testimonials.vue'
import Contact from '@/components/Contact.vue'
import Footer from '@/components/Footer.vue'
</script>

<template>
  <Header />
  <body>
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
    <CaseStudies />
    <Divider
      title="Our Working Process"
      text="Step-by-Step Guide to Achieving Your Business Goals"
      :max-width="300"
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
  </body>
  <Footer />
</template>

<style lang="scss">
#app {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: auto;
  max-width: 1240px;

  body {
    width: 100%;
  }
}

@media only screen and (max-width: 1280px) {
  #app {
    max-width: 85vw;
    overflow: hidden;
  }
}
</style>

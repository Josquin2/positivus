<script setup lang="ts">
import OneTeamMember from '@/components/OneTeamMember.vue'

const team = [
  {
    image: '/team/members/john-smith.png',
    name: 'John Smith',
    position: 'CEO and Founder',
    text: '10+ years of experience in digital marketing. Expertise in SEO, PPC, and content strategy'
  },
  {
    image: '/team/members/jane-doe.png',
    name: 'Jane Doe',
    position: 'Director of Operations',
    text: '7+ years of experience in project management and team leadership. Strong organizational and communication skills'
  },
  {
    image: '/team/members/michael-brown.png',
    name: 'Michael Brown',
    position: 'Senior SEO Specialist',
    text: '5+ years of experience in SEO and content creation. Proficient in keyword research and on-page optimization'
  },
  {
    image: '/team/members/emily-johnson.png',
    name: 'Emily Johnson',
    position: 'PPC Manager',
    text: '3+ years of experience in paid search advertising. Skilled in campaign management and performance analysis'
  },
  {
    image: 'team/members/brian-williams.png',
    name: 'Brian Williams',
    position: 'Social Media Specialist',
    text: '4+ years of experience in social media marketing. Proficient in creating and scheduling content, analyzing metrics, and building engagement'
  },
  {
    image: 'team/members/sarah-kim.png',
    name: 'Sarah Kim',
    position: 'Content Creator',
    text: '2+ years of experience in writing and editing Skilled in creating compelling, SEO-optimized content for various industries'
  }
]
</script>

<template>
  <div class="all-team-members">
    <OneTeamMember
      v-for="one in team"
      :image="one.image"
      :name="one.name"
      :position="one.position"
      :text="one.text"
    />
  </div>
</template>

<style lang="scss">
.all-team-members {
  margin-top: 80px;
  display: flex;
  flex-wrap: wrap;
  gap: 40px;
}
</style>

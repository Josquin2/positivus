<script setup lang="ts">
const props = defineProps({
  title: String,
  image: String,
  backgroundTitle: String,
  color: String
})

const colors = {
  gray: {
    background: '#f3f3f3',
    arrow: '/services/arrows/black.png',
    font: '#000000'
  },
  green: {
    background: '#b9ff66',
    arrow: '/services/arrows/black.png',
    font: '#000000'
  },
  black: {
    background: '#191a23',
    arrow: '/services/arrows/white.png',
    font: '#ffffff'
  },
  white: {
    background: '#ffffff',
    arrow: '/services/arrows/white.png',
    font: '#000000'
  }
}
</script>

<template>
  <div class="one-service" :style="`background-color:${colors[props.color].background}`">
    <div class="left">
      <h3 :style="`background-color:${colors[props.backgroundTitle].background}`">
        {{ props.title }}
      </h3>

      <div class="learn-more">
        <img :src="colors[props.color].arrow" alt="" />
        <p :style="`color:${colors[props.color].font}`">Learn more</p>
      </div>
    </div>
    <div class="right">
      <img :src="props.image" alt="" />
    </div>
  </div>
</template>

<style lang="scss">
.one-service {
  height: 310px;
  width: 600px;
  padding: 50px;
  border: 1px solid #000000;
  border-bottom: 5px solid #000000;
  border-radius: 45px;
  display: flex;
  align-items: center;
  justify-content: space-between;

  .left {
    height: 100%;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: space-between;

    h3 {
      max-width: 221px;
      font-size: 30px;
      font-weight: 400;
      border-radius: 7px;
      padding-left: 7px;
    }

    .learn-more {
      display: flex;
      align-items: center;
      gap: 15px;

      img {
        zoom: 0.5;
      }

      p {
        font-size: 20px;
      }
    }
  }

  .right {
    img {
      zoom: 0.5;
    }
  }
}
</style>

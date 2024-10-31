<script setup lang="ts">
const props = defineProps<{
  title: string
  image: string
  backgroundTitle: keyof typeof colors
  color: keyof typeof colors
}>()

const colors = {
  gray: {
    background: '#f3f3f3',
    arrow: 'services/arrows/black.png',
    font: '#000000'
  },
  green: {
    background: '#b9ff66',
    arrow: 'services/arrows/black.png',
    font: '#000000'
  },
  black: {
    background: '#191a23',
    arrow: 'services/arrows/white.png',
    font: '#ffffff'
  },
  white: {
    background: '#ffffff',
    arrow: 'services/arrows/white.png',
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
  max-width: 600px;
  width: 43vw;
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
      cursor: pointer;
      display: flex;
      align-items: center;
      gap: 15px;
      transition: 0.2s;

      img {
        zoom: 0.5;
      }

      p {
        font-size: 20px;
      }
    }

    .learn-more:hover {
      transform: scale(1.1);
    }
  }

  .right {
    img {
      zoom: 0.5;
    }
  }
}

@media only screen and (max-width: 1280px) {
  .one-service {
    width: 40vw;
    padding: 35px;
    position: relative;

    .left {
      h3 {
        position: absolute;
      }

      .learn-more {
        position: absolute;
        bottom: 35px;

        p {
          display: none;
        }
      }
    }

    .right {
      align-self: flex-end;

      img {
        max-width: 350px;
      }
    }
  }
}

@media only screen and (max-width: 950px) {
  .one-service {
    width: 100%;
    max-width: 100%;

    .left {
      .learn-more {
        p {
          display: block;
        }
      }
    }
  }
}

@media only screen and (max-width: 470px) {
  .one-service {
    width: 100vw;
    max-width: 390px;
    padding: 35px;
    position: relative;

    .left {
      h3 {
        font-size: 26px;
        position: absolute;
      }

      .learn-more {
        position: absolute;
        bottom: 35px;
        p {
          display: none;
        }
      }
    }

    .right {
      align-self: flex-end;
      img {
        max-width: 330px;
      }
    }
  }
}
</style>

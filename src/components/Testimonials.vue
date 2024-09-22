<script setup lang="ts">
import { ref } from 'vue'
import WhiteArrow from '@/components/icons/WhiteArrow.vue'
import PageIcon from '@/components/icons/PageIcon.vue'
const cards = [
  {
    author: 'John Smith5',
    position: 'Marketing Director at XYZ Corp',
    words:
      '"We have been working with Positivus for the past year and have seen a significant increase in website traffic and leads as a result of their efforts. The team is professional, responsive, and truly cares about the success of our business. We highly recommend Positivus to any company looking to grow their online presence."'
  },
  {
    author: 'John Smith1',
    position: 'Marketing Director at XYZ Corp',
    words:
      '"We have been working with Positivus for the past year and have seen a significant increase in website traffic and leads as a result of their efforts. The team is professional, responsive, and truly cares about the success of our business. We highly recommend Positivus to any company looking to grow their online presence."'
  },
  {
    author: 'John Smith2',
    position: 'Marketing Director at XYZ Corp',
    words:
      '"We have been working with Positivus for the past year and have seen a significant increase in website traffic and leads as a result of their efforts. The team is professional, responsive, and truly cares about the success of our business. We highly recommend Positivus to any company looking to grow their online presence."'
  },
  {
    author: 'John Smith3',
    position: 'Marketing Director at XYZ Corp',
    words:
      '"We have been working with Positivus for the past year and have seen a significant increase in website traffic and leads as a result of their efforts. The team is professional, responsive, and truly cares about the success of our business. We highly recommend Positivus to any company looking to grow their online presence."'
  },
  {
    author: 'John Smith4',
    position: 'Marketing Director at XYZ Corp',
    words:
      '"We have been working with Positivus for the past year and have seen a significant increase in website traffic and leads as a result of their efforts. The team is professional, responsive, and truly cares about the success of our business. We highly recommend Positivus to any company looking to grow their online presence."'
  },
  {
    author: 'John Smith5',
    position: 'Marketing Director at XYZ Corp',
    words:
      '"We have been working with Positivus for the past year and have seen a significant increase in website traffic and leads as a result of their efforts. The team is professional, responsive, and truly cares about the success of our business. We highly recommend Positivus to any company looking to grow their online presence."'
  },
  {
    author: 'John Smith1',
    position: 'Marketing Director at XYZ Corp',
    words:
      '"We have been working with Positivus for the past year and have seen a significant increase in website traffic and leads as a result of their efforts. The team is professional, responsive, and truly cares about the success of our business. We highly recommend Positivus to any company looking to grow their online presence."'
  }
]

const translate = ref(-346)

const currentPage = ref(0)

function onNextClick() {
  if (currentPage.value < 4) {
    currentPage.value += 1
    translate.value -= 656
  }
}

function onPrevClick() {
  if (currentPage.value > 0) {
    currentPage.value -= 1
    translate.value += 656
  }
}

function onPageClick(index: number) {
  if (currentPage.value < index) {
    translate.value -= (index - currentPage.value) * 656
  } else if (currentPage.value > index) {
    translate.value += (currentPage.value - index) * 656
  }
  currentPage.value = index
}
</script>

<template>
  <div class="testimonials-block">
    <div class="carousel">
      <div class="cards" :style="`transform: translateX(calc(${translate}px))`">
        <div class="one-card" v-for="card in cards">
          <div class="words">{{ card?.words }}</div>
          <div class="author">
            <h6>{{ card?.author }}</h6>
            <p>{{ card?.position }}</p>
          </div>
        </div>
      </div>
      <div class="navigation">
        <button @click="onPrevClick()" class="arrow" :class="{ 'disabled-arrow': currentPage < 1 }">
          <WhiteArrow class="left-arrow" />
        </button>
        <div class="pages">
          <button
            class="one-page"
            :class="{ 'current-page': currentPage == index }"
            v-for="(page, index) in cards.length - 2"
            :key="index"
            @click="onPageClick(index)"
          >
            <PageIcon />
          </button>
        </div>
        <button @click="onNextClick()" class="arrow" :class="{ 'disabled-arrow': currentPage > 3 }">
          <WhiteArrow class="right-arrow" />
        </button>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
.testimonials-block {
  margin-top: 80px;

  .carousel {
    max-width: 1240px;
    width: 100%;
    padding: 84px 0px 68px 0px;
    background-color: #191a23;
    border-radius: 45px;
    min-height: 625px;
    overflow: hidden;
    display: flex;
    flex-direction: column;
    justify-content: space-between;

    .cards {
      display: flex;
      gap: 50px;
      transition: 0.5s;

      .one-card {
        min-width: 606px;

        .words {
          color: #ffffff;
          border: 1px solid #b9ff66;
          border-radius: 45px;
          position: relative;
          padding: 48px 52px;
        }

        .author {
          margin-left: 75px;
          margin-top: 48px;
          h6 {
            color: #b9ff66;
            font-size: 20px;
            font-weight: 300;
          }
          p {
            color: #ffffff;
            font-size: 18px;
          }
        }
        .words::after {
          content: '';
          position: absolute;
          bottom: -21.2px;
          left: 60px;
          width: 40px;
          height: 40px;
          border: 1px solid #b9ff66;
          border-top: none;
          border-left: none;
          background-color: #191a23;
          rotate: 45deg;
        }
      }
    }

    .navigation {
      display: flex;
      justify-content: center;
      gap: 180px;

      .arrow {
        transition: 0.2s;
        cursor: pointer;
        background-color: transparent;
        border: none;

        .left-arrow {
          rotate: 180deg;
        }
      }
      .disabled-arrow {
        cursor: default;
        opacity: 30%;
      }

      .pages {
        display: flex;
        align-items: center;
        gap: 20px;

        .one-page {
          display: flex;
          cursor: pointer;
          background-color: transparent;
          border: none;
        }

        .current-page {
          cursor: default;
          svg {
            path {
              fill: #b9ff66;
            }
          }
        }
      }
    }
  }
}
</style>

<script setup lang="ts">
import { ref } from 'vue'
import WhiteArrow from '@/components/icons/WhiteArrow.vue'
import PageIcon from '@/components/icons/PageIcon.vue'
const cards = [
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
  }
]

const translate = ref(0)

const currentPage = ref(0)

function onNextClick() {
  if (currentPage.value < 4) {
    currentPage.value += 1
    translate.value -= 120
  }
}

function onPrevClick() {
  if (currentPage.value > 0) {
    currentPage.value -= 1
    translate.value += 120
  }
}

function onPageClick(index: number) {
  if (currentPage.value < index) {
    translate.value -= (index - currentPage.value) * 120
  } else if (currentPage.value > index) {
    translate.value += (currentPage.value - index) * 120
  }
  currentPage.value = index
}
</script>

<template>
  <div class="testimonials-block-m">
    <div class="carousel">
      <div class="cards" :style="`transform: translateX(${translate}%)`">
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
            v-for="(page, index) in cards.length"
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
.testimonials-block-m {
  display: none;
  margin-top: 40px;

  .carousel {
    width: 100%;
    padding: 70px 110px 60px 110px;
    min-height: 454px;
    gap: 60px;

    .cards {
      gap: 0px;

      .one-card {
        min-width: 100%;
        margin-right: 20%;

        .words {
          border-radius: 40px;
          padding: 30px;
          font-size: 16px;
          font-weight: 100;
        }
        .author {
          margin-left: 60px;
          margin-top: 45px;
          h6 {
            font-size: 16px;
          }
          p {
            font-size: 14px;
          }
        }
      }
      .words::after {
        left: 48px;
      }
    }

    .navigation {
      gap: 0px;
      justify-content: space-between;

      .pages {
        gap: 17px;
      }

      .arrow {
        zoom: 0.83;
      }
    }
  }
}

@media only screen and (max-width: 1280px) {
  .testimonials-block-xl {
    display: none;
  }

  .testimonials-block-m {
    display: flex;

    .carousel {
      height: fit-content;
      .navigation {
        justify-content: space-around;
      }
    }
  }
}

@media only screen and (max-width: 800px) {
  .testimonials-block-m {
    .carousel {
      padding: 30px 30px 60px 30px;
      .navigation {
        justify-content: space-between;
      }
    }
  }
}
</style>

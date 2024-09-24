<script setup lang="ts">
import ShortLine from '@/components/icons/ShortLine.vue'
const props = defineProps({
  id: Number,
  title: String,
  text: String
})

function onMoreClick(id: String) {
  document.getElementById(id)?.classList.toggle('extended')
}
</script>

<template>
  <div
    class="one-working-process"
    :id="`process-${props?.id}`"
    @click="onMoreClick('process-' + props.id)"
  >
    <div class="up">
      <div class="title">
        <h1>{{ '0' + (props.id + 1) }}</h1>
        <h4>{{ props.title }}</h4>
      </div>
      <div class="button">
        <button>
          <div class="sign">
            <ShortLine class="rotated" />
            <ShortLine />
          </div>
        </button>
      </div>
    </div>
    <div class="divider"></div>
    <div class="bottom">
      <p>{{ props.text }}</p>
    </div>
  </div>
</template>

<style lang="scss">
.one-working-process {
  overflow: hidden;
  height: 159px;
  width: 100%;
  background-color: #f3f3f3;
  border: 1px solid #000000;
  border-bottom: 6px solid #000000;
  border-radius: 45px;
  padding: 41px 60px;
  transition: 0.5s;

  .up {
    display: flex;
    align-items: center;
    justify-content: space-between;
    cursor: default;
    .title {
      display: flex;
      align-items: center;
      h1 {
        font-size: 60px;
        font-weight: 400;
      }

      h4 {
        margin-left: 25px;
        font-size: 30px;
        font-weight: 300;
      }
    }

    .button {
      button {
        cursor: pointer;
        width: 58px;
        height: 58px;
        border-radius: 50%;
        border: 1px solid #000000;
        background-color: #f3f3f3;
        display: flex;
        align-items: center;
        justify-content: center;

        .sign {
          span {
            transition: 0.6s;
          }
          .rotated {
            position: absolute;
            animation-name: rotate-from;
            animation-duration: 0.5s;
            rotate: 90deg;
          }
        }
      }
    }
  }

  .divider {
    transition: 0.5s;
    opacity: 0;
    width: 100%;
    margin: 30px 0px;
    height: 1px;
    background-color: #000000;
  }

  .bottom {
    transition: 0.5s;
    opacity: 0;
  }
}
.extended {
  background-color: #b9ff66;
  height: 279px;

  .up {
    .button {
      button {
        .sign {
          span {
            width: 17.7px;
          }
          .rotated {
            animation-name: rotate-to;
            animation-duration: 0.5s;
            rotate: 0deg;
          }
        }
      }
    }
  }

  .divider {
    opacity: 100%;
  }
  .bottom {
    opacity: 100%;
  }
}

@media only screen and (max-width: 800px) {
  .extended {
    height: 230px !important;
  }
  .one-working-process {
    height: 98px;
    padding: 30px;
    .up {
      .title {
        h1 {
          font-size: 28px;
        }
        h4 {
          margin-left: 10px;
          font-size: 16px;
        }
      }
      .button {
        button {
          width: 30px;
          height: 30px;

          .sign {
            .short-line-25 {
              width: 13px;
              height: 4px;
            }
          }
        }
      }
    }
  }
}

@media only screen and (max-width: 700px) {
  .extended {
    height: 300px !important;
  }
}

@media only screen and (max-width: 420px) {
  .extended {
    height: 350px !important;
  }
}
</style>

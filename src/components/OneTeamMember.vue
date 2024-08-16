<script setup lang="ts">
const props = defineProps({
  image: String,
  name: String,
  position: String,
  text: String
})
</script>

<template>
  <div class="one-team-member">
    <div class="up">
      <div class="about">
        <div class="photo">
          <img :src="props.image" alt="" />
        </div>
        <div class="short-info">
          <h2>{{ props.name }}</h2>
          <h4>{{ props.position }}</h4>
        </div>
      </div>
      <div class="in">
        <img src="/team/in.png" alt="" />
      </div>
    </div>
    <div class="divider"></div>
    <div class="down">
      <p>{{ props.text }}</p>
    </div>
  </div>
</template>

<style lang="scss">
.one-team-member {
  height: 362px;
  width: 387px;
  padding: 40px 35px;
  display: flex;
  flex-direction: column;
  border: 1px solid #000000;
  border-bottom: 6px solid #000000;
  border-radius: 45px;

  .up {
    display: flex;
    justify-content: space-between;

    .about {
      display: flex;
      gap: 20px;
      .photo {
        display: flex;
        align-self: center;
        img {
          zoom: 0.5;
        }
      }

      .short-info {
        align-self: flex-end;

        h2 {
          font-size: 20px;
        }
        h4 {
          font-size: 18px;
          font-weight: 200;
        }
      }
    }

    .in {
      align-self: flex-start;

      img {
        zoom: 0.5;
      }
    }
  }

  .divider {
    margin: 28px 0px;
    width: 100%;
    height: 1px;
    background-color: #000000;
  }

  .down {
    max-width: 317px;

    p {
      font-size: 18px;
      font-weight: 200;
    }
  }
}
</style>

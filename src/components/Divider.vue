<script setup lang="ts">
const props = defineProps({
  title: String,
  text: String,
  maxWidth: Number
})
</script>

<template>
  <div class="divider">
    <h2>{{ props.title }}</h2>
    <h6 :style="`max-width:${props.maxWidth}px`">{{ props.text }}</h6>
  </div>
</template>

<style lang="scss">
.divider {
  margin-top: 140px;
  display: flex;
  gap: 40px;
  align-items: center;

  h2 {
    font-size: 40px;
    padding: 0px 7px;
    background-color: #b9ff66;
    border-radius: 7px;
    font-weight: 300;
  }

  h6 {
    font-size: 18px;
    font-weight: 200;
  }
}

@media only screen and (max-width: 800px) {
  .divider {
    margin-top: 60px;
    flex-direction: column;
    gap: 30px;

    h2 {
      text-align: center;
      font-size: 36px;
    }

    h6 {
      font-size: 16px;
    }
  }
}
</style>

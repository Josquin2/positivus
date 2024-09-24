<script setup lang="ts">
import GreenArrow from '@/components/icons/GreenArrow.vue'
</script>

<template>
  <div class="case-studies-block">
    <div class="one-case">
      <h5>
        For a local restaurant, we implemented a targeted PPC campaign that resulted in a 50%
        increase in website traffic and a 25% increase in sales.
      </h5>
      <button>
        <p>Learn more</p>
        <GreenArrow />
      </button>
    </div>
    <hr />
    <div class="one-case">
      <h5>
        For a B2B software company, we developed an SEO strategy that resulted in a first page
        ranking for key keywords and a 200% increase in organic traffic.
      </h5>
      <button>
        <p>Learn more</p>
        <GreenArrow />
      </button>
    </div>
    <hr />
    <div class="one-case">
      <h5>
        For a national retail chain, we created a social media marketing campaign that increased
        followers by 25% and generated a 20% increase in online sales.
      </h5>
      <button>
        <p>Learn more</p>
        <GreenArrow />
      </button>
    </div>
  </div>
</template>

<style lang="scss">
.case-studies-block {
  margin-top: 80px;
  padding: 60px 70px;
  background-color: #191a23;
  border-radius: 45px;
  display: flex;
  gap: 64px;

  .one-case {
    display: flex;
    flex-direction: column;
    height: fit-content;
    h5 {
      color: #ffffff;
      font-size: 18px;
      font-weight: 200;
    }

    button {
      cursor: pointer;
      margin-top: 20px;
      display: flex;
      gap: 15px;
      background-color: transparent;
      border: none;

      p {
        color: #b9ff66;
        font-size: 20px;
        letter-spacing: 1px;
      }
    }
  }
}

@media only screen and (max-width: 1100px) {
  .case-studies-block {
    margin-top: 40px;
    overflow: scroll;
    background-color: #ffffff;
    padding: 0;
    border-radius: 0;
    gap: 20px;
    .one-case {
      width: 350px;
      height: auto;
      background-color: #191a23;
      padding: 42px 50px;
      border-radius: 45px;

      h5 {
        max-width: 250px;
        width: 80vw;
        font-size: 16px;
      }
    }
    hr {
      display: none;
    }
  }
}
</style>

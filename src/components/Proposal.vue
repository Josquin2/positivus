<template>
  <div class="proposal-block">
    <div class="left">
      <h4>Let’s make things happen</h4>
      <p>
        Contact us today to learn more about how our digital marketing services can help your
        business grow and succeed online.
      </p>
      <button>Get your free proposal</button>
    </div>
    <div class="right">
      <img src="/images/proposal.png" alt="" />
    </div>
  </div>
</template>

<style lang="scss">
.proposal-block {
  width: 100%;
  height: 347px;
  background-color: #f3f3f3;
  border-radius: 45px;
  margin-top: 100px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 60px;

  .left {
    max-width: 500px;
    height: 100%;
    display: flex;
    flex-direction: column;
    gap: 26px;

    h4 {
      font-size: 30px;
    }

    p {
      font-size: 18px;
      font-weight: 300;
    }
    button {
      cursor: pointer;
      width: fit-content;
      padding: 20px 35px;
      background-color: #191a23;
      color: #ffffff;
      font-size: 20px;
      font-weight: 300;
      border: 0px solid #191a23;
      border-radius: 14px;
      transition: 0.2s;
    }
    button:hover {
      background-color: #b9ff66;
      color: #000000;
      border-bottom: 8px solid #191a23;
    }
  }
  .right {
    margin-right: 75px;
    img {
      zoom: 0.5;
    }
  }
}

@media only screen and (max-width: 1280px) {
  .proposal-block {
    .right {
      margin-right: 0;
    }
  }
}

@media only screen and (max-width: 1040px) {
  .proposal-block {
    .right {
      img {
        zoom: 0.3;
      }
    }
  }
}

@media only screen and (max-width: 950px) {
  .proposal-block {
    .right {
      display: none;
    }
  }
}

@media only screen and (max-width: 650px) {
  .proposal-block {
    margin-top: 40px;
    padding: 35px;

    .left {
      height: auto;
      flex-direction: column;
      align-items: center;
      h4 {
        font-size: 26px;
      }

      p {
        font-size: 16px;
      }
      button {
        font-size: 16px;
      }
    }
  }
}
</style>

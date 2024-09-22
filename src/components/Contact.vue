<template>
  <div class="contact-block">
    <div class="left">
      <div class="checkboxes"></div>
      <div class="inputs">
        <div>
          <p>Name</p>
          <input type="text" name="" id="" />
        </div>
        <div>
          <p>Email*</p>
          <input type="text" name="" id="" />
        </div>
        <div>
          <p>Message*</p>
          <textarea name="" id="" cols="30" rows="10"></textarea>
        </div>
      </div>
      <div class="button">
        <button>Send Message</button>
      </div>
    </div>
    <div class="right">
      <img src="/contact/image.png" alt="" />
    </div>
  </div>
</template>

<style lang="scss">
.contact-block {
  margin-top: 80px;
  background-color: #f3f3f3;
  width: 100%;
  height: fit-content;
  padding: 60px 0px 80px 100px;
  border-radius: 45px;
  display: flex;
  align-items: center;
  justify-content: space-between;

  .left {
    display: flex;
    flex-direction: column;
    gap: 40px;
    width: 556px;

    .inputs {
      display: flex;
      flex-direction: column;
      gap: 25px;

      div {
        p {
          font-size: 16px;
          font-weight: 200;
        }
        input,
        textarea {
          border: 1px solid #000000;
          border-radius: 14px;
          padding-left: 30px;
          height: 59px;
          width: 100%;
          margin-top: 5px;
          font-size: 18px;
        }

        textarea {
          height: 190px;
          resize: none;
          padding: 18px 30px;
        }
      }
    }

    .button {
      button {
        cursor: pointer;
        width: 100%;
        background-color: #191a23;
        color: #ffffff;
        height: 68px;
        border: none;
        border-radius: 14px;
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

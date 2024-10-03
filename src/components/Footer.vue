<template>
  <footer class="footer">
    <div class="top">
      <div class="logo">
        <img src="/footer/logo.png" alt="" />
      </div>
      <div class="links">
        <button>About us</button>
        <button>Services</button>
        <button>Use Cases</button>
        <button>Pricing</button>
        <button>Blog</button>
      </div>
      <div class="social">
        <img src="/footer/in.png" alt="" />
        <img src="/footer/f.png" alt="" />
        <img src="/footer/x.png" alt="" />
      </div>
    </div>
    <div class="middle">
      <div class="left">
        <h6>Contact us:</h6>
        <div class="contacts">
          <p>Email: info@positivus.com</p>
          <p>Phone: 555-567-8901</p>
          <p>Address: 1234 Main St Moonstone City, Stardust State 12345</p>
        </div>
      </div>
      <div class="right">
        <input type="text" placeholder="Email" />
        <button>Subscribe to news</button>
      </div>
    </div>
    <div class="divider-line"></div>
    <div class="bottom">
      <p>© 2023 Positivus. All Rights Reserved.</p>
      <a>Privacy Policy</a>
    </div>
  </footer>
</template>

<style lang="scss">
.footer {
  width: 100%;
  margin: 140px 0px 0px 0px;
  padding: 55px 60px 50px 60px;
  background-color: #191a23;
  border-radius: 45px 45px 0px 0px;
  display: flex;
  flex-direction: column;
  gap: 50px;

  .top {
    display: flex;
    align-items: center;
    justify-content: space-between;
    .logo {
      img {
        zoom: 0.5;
      }
    }

    .links {
      display: flex;
      gap: 40px;

      button {
        cursor: pointer;
        background-color: transparent;
        border: none;
        font-size: 18px;
        border-bottom: 1px solid transparent;
        transition: 0.2s ease-in;
      }
      button:hover {
        border-bottom: 1px solid #ffffff;
      }
    }
    .social {
      display: flex;
      gap: 20px;
      img {
        cursor: pointer;
        zoom: 0.5;
      }
    }
  }

  .middle {
    display: flex;
    align-items: center;
    justify-content: space-between;

    .left {
      max-width: 333px;
      display: flex;
      flex-direction: column;
      gap: 27px;

      h6 {
        font-size: 20px;
        padding: 0px 7px;
        width: fit-content;
        background-color: #b9ff66;
        border-radius: 7px;
        color: #191a23;
      }

      .contacts {
        display: flex;
        flex-direction: column;
        gap: 20px;

        p {
          font-size: 18px;
          font-weight: 200;
        }
      }
    }

    .right {
      background-color: #292a32;
      border-radius: 14px;
      width: fit-content;
      padding: 58px 40px;
      display: flex;
      align-items: center;
      gap: 20px;

      button {
        cursor: pointer;
        padding: 20px 35px;
        background-color: #b9ff66;
        color: #191a23;
        border-radius: 14px;
        border: none;
        font-size: 20px;
        font-weight: 200;
        text-wrap: nowrap;
      }
      input {
        min-width: 285px;
        border: 1px solid #ffffff;
        padding: 22px 0px 22px 35px;
        background-color: transparent;
        border-radius: 14px;
        font-size: 18px;
      }
    }
  }

  .divider-line {
    width: 100%;
    height: 1px;
    background-color: #ffffff;
  }

  .bottom {
    display: flex;
    align-items: center;
    gap: 40px;

    a,
    p {
      font-size: 18px;
      font-weight: 200;
    }

    a {
      cursor: pointer;
      border-bottom: 1px solid #ffffff;
    }
  }

  * {
    color: #ffffff;
  }
}

@media only screen and (max-width: 1180px) {
  .footer {
    .middle {
      .right {
        flex-direction: column;
        padding: 58px 80px;

        input,
        button {
          width: 290px;
        }
      }
    }
  }
}

@media only screen and (max-width: 1120px) {
  .footer {
    .top {
      .social {
        display: none;
      }
    }
  }
}

@media only screen and (max-width: 960px) {
  .footer {
    .top {
      flex-direction: column;
      gap: 37px;
    }
  }
}

@media only screen and (max-width: 900px) {
  .footer {
    .middle {
      flex-direction: column;
      gap: 37px;

      .left {
        h6 {
          width: 100%;
        }
        * {
          text-align: center !important;
        }
      }
    }
  }
}

@media only screen and (max-width: 750px) {
  .footer {
    width: 100vw;
  }
}

@media only screen and (max-width: 630px) {
  .footer {
    margin-top: 90px;
    border-radius: 0;

    .top {
      .links {
        flex-direction: column;
      }
    }

    .middle {
      .left {
        align-items: center;

        h6 {
          width: fit-content;
        }
      }
    }

    .bottom {
      flex-direction: column;
      gap: 15px;
    }
  }
}

@media only screen and (max-width: 500px) {
  .footer {
    padding: 50px 20px 30px 20px;

    .top {
      .links {
        gap: 15px;
      }
    }

    .middle {
      .right {
        padding: 30px;
      }
    }
  }
}
</style>

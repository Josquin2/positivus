<script setup lang="ts">
import Header from '@/components/Header.vue'
import FirstView from '@/components/FirstView.vue'
import Logotypes from '@/components/Logotypes.vue'
import Divider from '@/components/Divider.vue'
import AllServices from '@/components/AllServices.vue'
import Proposal from '@/components/Proposal.vue'
import CaseStudies from '@/components/CaseStudies.vue'
import AllWorking from '@/components/AllWorking.vue'
import TeamMembers from '@/components/TeamMembers.vue'
import Testimonials from '@/components/Testimonials.vue'
import Contact from '@/components/Contact.vue'
</script>

<template>
  <div class="positivus-main-page">
    <Header />
    <body>
      <FirstView />
      <Logotypes />
      <Divider
        title="Services"
        text="At our digital marketing agency, we offer a range of services to help businesses grow and succeed online. These services include:"
        :max-width="580"
      />
      <AllServices />
      <Proposal />
      <Divider
        title="Case Studies"
        text="Explore Real-Life Examples of Our Proven Digital Marketing Success through Our Case Studies"
        :max-width="580"
      />
      <CaseStudies />
      <Divider
        title="Our Working Process"
        text="Step-by-Step Guide to Achieving Your Business Goals"
        :max-width="300"
      />
      <AllWorking />
      <Divider
        title="Team"
        text="Meet the skilled and experienced team behind our successful digital marketing strategies"
        :max-width="473"
      />
      <TeamMembers />
      <Divider
        title="Testimonials"
        text="Hear from Our Satisfied Clients: Read Our Testimonials to Learn More about Our Digital Marketing Services"
        :max-width="473"
      />
      <Testimonials />
      <Divider
        title="Contact Us"
        text="Connect with Us: Let's Discuss Your Digital Marketing Needs"
        :max-width="323"
      />
      <Contact />
    </body>
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
  </div>
</template>

<style lang="scss">
.positivus-main-page {
  display: flex;
  flex-direction: column;
  width: 1440px;
  margin: auto;
}
.footer {
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
</style>

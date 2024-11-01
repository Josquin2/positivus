<script setup lang="ts">
function onHamburgerClick() {
  document?.getElementById('nav-phone')?.classList?.toggle('nav-closed')
  document?.getElementById('nav-phone')?.classList?.toggle('nav-opened')
}
</script>

<template>
  <header class="main-page-header" id="main-page-header">
    <div class="header-logo">
      <img src="/header/logo.png" alt="" />
    </div>
    <div class="header-links">
      <button class="one__link">About us</button>
      <button class="one__link">Services</button>
      <button class="one__link">Use Cases</button>
      <button class="one__link">Pricing</button>
      <button class="one__link">Blog</button>
      <button class="one__link header--button">Request a quote</button>
    </div>
    <div class="header-links-phone nav-closed" id="nav-phone">
      <button class="hamburger" @click="onHamburgerClick()">
        <span class="top"></span>
        <span class="center"></span>
        <span class="bottom"></span>
      </button>
      <div class="nav-phone">
        <div class="header-links">
          <button class="one__link">About us</button>
          <button class="one__link">Services</button>
          <button class="one__link">Use Cases</button>
          <button class="one__link">Pricing</button>
          <button class="one__link">Blog</button>
          <button class="one__link header--button">Request a quote</button>
        </div>
      </div>
    </div>
  </header>
</template>

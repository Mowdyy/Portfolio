<template>
  <div id="app">
    <!-- <div class="header">
      <nav>
        <router-link to="/home" class="items">Home</router-link> |
        <router-link to="/about" class="items">About</router-link> |
        <router-link to="/projects" class="items">Projects</router-link>        
      </nav>
    </div> -->
    <main class="App__main">
      <transition
        name="fade"
        mode="out-in"
      >
        <router-view/>
      </transition>
    </main>
    <Footer />
  </div>
</template>

<script>
import Footer from '@/components/Footer.vue'

export default {
  name: 'App',
  components: {
    Footer
  }
}
</script>

<style>
@font-face {
  font-family: "Raleway-Reg";
  src: url("./assets/fonts/Raleway/Raleway-Regular.ttf");
}
@font-face {
  font-family: "Raleway-EB";
  src: url("./assets/fonts/Raleway/Raleway-ExtraBold.ttf");
}

body {
  margin: 0;
  padding: 0;
}

.fade-enter-active,
.fade-leave-active {
  transition-duration: 0.3s;
  transition-property: opacity;
  transition-timing-function: ease;
}

.fade-enter,
.fade-leave-active {
  opacity: 0
}

.header {
  width: 100vw;
  height: 100px;
  display: flex;
  justify-content: flex-end;
  position: fixed;
}

a {
  font-family: Raleway-Reg;
  color: white;
  text-decoration: none;
  font-size: 16px;
  margin: 0 40px;
}

nav {
  display: flex;
  align-items: center;
  padding: 0 20px;
  color: white;
}

.items:hover {
  color: #694CD4;
}

@media screen and (max-width: 900px) {
  nav {
    display: none;
  }
}
</style>

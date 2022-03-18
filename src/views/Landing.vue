<template>
  <div class="landing">
    <transition name="fade" mode="out-in">
      <div class="welcome-content">
        <p>Bienvenue, Je suis</p>
        <h1>Benoît Favrie</h1>
        <router-link to="/home">
          <div class="button">
            <Button placeholder="See my Portfolio"/>
          </div>
        </router-link>
        <p class="intel">Veuillez noter que ce site est encore en cours de développement...</p>
      </div>
    </transition>
  </div>
  
</template>

<script>

import Button from '@/components/Button.vue'

export default {
  name: 'Landing',
  components: {
    Button
  },
  methods: {
  }
}
</script>

<style scoped>
body, html {
  margin: 0;
  padding: 0;
}

.intel {
  margin: 20px 0;
  font-style: italic;
}

.landing {
  margin: 0;
  width: 100vw;
  height: 100vh;
  font-family: Raleway;
  background-color: #3F5288;
  color: white;
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s ease;
}


.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}

.welcome-content {
  height: 100%;
  width: 100%;
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
  transition: opacity 1s;
}

p {
  margin: 0;
}

h1 {
  margin: 20px 0;
}


@media screen and (min-width: 900px) {
  h1 {
    font-size: 3.5rem;
  }
}
</style>

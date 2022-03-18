<template>
<div class="main">
  <section class="contact">
    <div class="intro">
      <h1>Prendre contact &#129488;</h1>
      <a href="mailto:benoit14.favrie@gmail.com" target="_blank">
        <Button placeholder="Me contacter par mail" />
      </a>
    </div>
  </section>
</div>
</template>

<script>

import Button from '@/components/Button.vue'

export default {
  name: 'Contact',
  components: {
    Button
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.main {
  display: flex;
  flex-direction: column;
  align-items: center;
  background: url("../assets/images/bg.png");
}

.contact {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 30vh;
  flex-wrap: wrap;
}

.intro {
  gap: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  color: white;
  font-family: Raleway;
}

</style>
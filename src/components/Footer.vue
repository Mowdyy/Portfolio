<template>
  <div class="footer">
    <p>version: 0.4</p>
  </div>
</template>

<script>

export default {
  name: 'Footer'
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.footer {
  width: 100vw;
  height: 100px;
  position: fixed;
  bottom: 0;
  left: 0;
  display: flex;
  justify-content: flex-start;
  align-items: center;
  font-family: Raleway-Reg;
  color: white;
  padding: 0 40px;
}

@media screen and (max-width: 800px) {
  .footer {
    display: none;
  }
}
</style>

<template>
  <button class="fill">
    {{ placeholder }}
  </button>
</template>

<script>
export default {
  name: 'Button',
  props: {
     placeholder: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
button {
  position: relative;
  display: block;
  margin: 0 !important;
  padding: 12px 20px;
  font-family: Raleway-EB;
  letter-spacing: 1px;
  color: white;
  border: 2px #694CD4 solid;
  border-radius: 4px;
  text-transform: uppercase;
  outline: 0;
  overflow:hidden;
  background: none;
  z-index: 1;
  cursor: pointer;
  transition:         0.08s ease-in;
  -o-transition:      0.08s ease-in;
  -ms-transition:     0.08s ease-in;
  -moz-transition:    0.08s ease-in;
  -webkit-transition: 0.08s ease-in;
  font-size: 12px;
}

.fill:before {
  content: "";
  position: absolute;
  background: #694CD4;
  bottom: 0;
  left: 0;
  right: 0;
  top: 100%;
  z-index: -1;
  margin: 0;
  -webkit-transition: top 0.09s ease-in;
}

.fill:hover:before {
  top: 0;
}
</style>

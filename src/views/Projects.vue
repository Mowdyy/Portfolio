<template>
<div class="main">
  <section class="projects">
    <div class="title-items">
      <h1>Mes Projets</h1>
      <p>Découvrez mes projets</p>
      <el-divider class="sub-title-divider"/>
      <p style="font-style: italic;">Vous pouvez cliquer sur les fiches avec une petite icône pour découvrir mon projet en détail</p>
    </div>
    <div class="content">
      <div class="item">
        <img class="link" src="@/assets/images/icons/link.svg">
        <a href="http://www.flow.raidghost.com/" target="_blank">
          <img class="item__image" src="@/assets/images/flow.svg" alt="Flow" />
        </a>
        <p style="font-weight: bold;">FLOW</p>
        <p>Nous avons réalisé Flow dans le cadre d'un projet de fin d'études pour notre formation. Je me suis occupé de la partie développement, en ajoutant quelques touches personnelles. &#128540;</p>
      </div>
      <div class="item">
        <img class="link" src="@/assets/images/icons/link.svg">
        <a href="https://github.com/Mowdyy/sunnyoak" target="_blank">
          <img class="item__image" src="@/assets/images/sunnyOak.svg" alt="" />
        </a>
        <p style="font-weight: bold;">SUNNYOAK</p>
        <p>Nous avons réalisé SunnyOak comme un projet personnel, le but était de créer une lampe de A à Z, et qui peut être gérée par une application que j'ai créée en JS. &#128523;</p>
      </div>
    </div>
  </section>
</div>
</template>

<script>

import Button from '@/components/Button.vue'

export default {
  name: 'Projects',
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
  background: rgb(63,82,136);
}

.projects {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  font-family: Raleway;
  min-height: 100vh;
  padding-bottom: 50px;
}

.content {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 40px;
  max-height: auto;
  max-width: 1000px;
  margin: 0 20px;
}

.item {
  display: flex;
  align-content: center;
  flex-direction: column;
  word-break: keep-all;
  text-align: justify;
  height: 500px;
  max-width: 300px;
  background-color: #384772;
  border-radius: 10px;
  position: relative;
  gap: 10px;
}

.item img:hover {
  opacity: 0.7;
  transition: all 0.2s linear;
}

.item p{
  color: white;
  padding: 0 20px;
}

.item img{
  width: 300px;
  height: 300px;
  border-radius: 10px;
}

.link {
  position: absolute;
  bottom: 10px;
  right: 15px;
  width: 15px !important;
}

.title-items {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  color: white;
  gap: 10px;
  padding: 0 20px;
  height: 280px;
}

.infos {
  display: flex;
}

.sub-title-divider {
  width: 20px;
  margin: 10px;
}

.section-divider {
  width: 80vw;
  margin: 10px;
  text-align: center;
}

</style>
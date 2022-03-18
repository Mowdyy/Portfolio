<template>
  <div class="main">
    <section class="home">
      <div class="home-container">
        <img class="logo" src="@/assets/images/logo.png">
        <div class="name">
          <h1>Benoît Favrie</h1>
          <p>Voici mon Portfolio</p>
          <img src="@/assets/images/profil.svg">
          <el-divider class="sub-title-divider" />
          <a href="mailto:benoit14.favrie@gmail.com" target="_blank">
            <Button placeholder="Me contacter" />
          </a>
        </div>
        <div class="intro">
          <p><b>INTRODUCTION</b></p>
          <h1 class="job">Front-End | Back-End Developer</h1>
          <el-divider class="sub-title-divider" />
          <p>Je suis en alternance à Caen en développement web. Je suis accepté à l'HETIC De Paris, et je souhaiterais intégrer une nouvelle entreprise pour la rentrée 2022.</p>
          <div class="block-radio">
            <el-timeline reverse>
              <el-timeline-item
                v-for="(activity, index) in activities"
                :key="index"
                :timestamp="activity.timestamp"
              >
                <p>{{activity.content}}</p>
              </el-timeline-item>
            </el-timeline>
          </div>
        </div>
      </div>
    </section>
    <About />
    <Projects />
    <Contact />
  </div>
</template>

<script>
import About from '@/views/About.vue';
import Projects from '@/views/Projects.vue';
import Contact from '@/views/Contact.vue';

import Button from '@/components/Button.vue';

export default {
  name: 'Home',
  components: {
    About,
    Projects,
    Button,
    Contact
  },
  data() {
      return {
        activities: [{
          content: "Baccalauréat S - Sciences de L'ingénieur",
          timestamp: '2020'
        }, {
          content: "DUT - Métiers du Multimédia et de l'Internet",
          timestamp: '2020-2022'
        }, {
          content: 'Admis à HETIC de Paris',
          timestamp: '2022'
        }]
      };
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
* {
  font-family: Raleway;
  margin: 0;
  padding: 0;
}

.home {
  background: no-repeat url("../assets/images/bg.png");
  background-color: #2F3956;
}

.logo {
  position: absolute;
  top: 20px;
  height: 7vh;
  left: 40px;
}

.home-container {
  color: white;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  gap: 300px;
  margin: 0 50px;
}

.intro {
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.name {
  display: flex;
  flex-direction: column;
  gap: 20px;
  align-items: center;
}

.name img {
  width: 200px;
  border-radius: 50%;
}

h1 {
  font-size: 4vh;
}

.job {
  color: #694CD4;
}

.home-container div {
  width: 500px;
}

.sub-title-divider {
  width: 20px !important;
}

.profil {
  width: 20vw;
}

.block-radio {
  max-width: 300px;
  margin-top: 40px;
}

.el-timeline-item p {
  color: white !important;
}

@media screen and (max-width: 1100px) {
  .home-container {
    padding: 200px 0;
    gap: 200px;
  }
}

@media screen and (min-width: 1100px) and (max-width: 1320px) {
  .home-container {
    padding: 200px 100px;
    gap: 200px;
  }
}

@media screen and (min-width: 1321px) and (max-width: 1420px) {
  .home-container {
    padding: 0;
    gap: 200px;
  }
}

@media screen and (max-width: 800px) {
  h1 {
    text-align: center;
  }
}


</style>
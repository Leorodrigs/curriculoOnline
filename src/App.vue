<template>
  <div class="background-image">
    <div class="container">
      <AppHeader />
      <Accordion
        title="Hard Skills"
        :isOpen="openAccordion === 'hard-skills'"
        @toggle="toggleAccordion('hard-skills')"
      >
        <HardSkills />
      </Accordion>
      <Accordion
        title="Soft Skills"
        :isOpen="openAccordion === 'soft-skills'"
        @toggle="toggleAccordion('soft-skills')"
      >
        <SoftSkills />
      </Accordion>
      <Accordion
        title="Portfólio e Currículo"
        :isOpen="openAccordion === 'portfolio'"
        @toggle="toggleAccordion('portfolio')"
      >
        <AppPortfolio />
      </Accordion>
    </div>
  </div>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";
import Accordion from "./components/Accordion.vue";
import HardSkills from "./components/HardSkills.vue";
import SoftSkills from "./components/SoftSkills.vue";
import AppPortfolio from "./components/AppPortfolio.vue";

export default {
  name: "App",
  components: {
    AppHeader,
    Accordion,
    HardSkills,
    SoftSkills,
    AppPortfolio,
  },
  data() {
    return {
      openAccordion: null,
    };
  },
  methods: {
    toggleAccordion(name) {
      this.openAccordion = this.openAccordion === name ? null : name;
    },
  },
};
</script>

<style>
body {
  font-family: "Poppins", sans-serif;
  color: rgb(0, 0, 0);
}

.background-image {
  background-image: url("./assets/Background.jpeg");
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
}

.container {
  background-image: url("./assets/Background1.jpeg");
  border-radius: 10px;
  padding: 20px;
  width: 800px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}


@media (max-width: 768px) {
  .container {  
  width: 600px;  
}
}

@media (max-width: 480px) {
  .container {  
  width: 400px;  
}
}


</style>

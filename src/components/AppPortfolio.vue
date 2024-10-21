<template>
  <app-accordion title="Portfólio e Currículo">
    <div class="portfolio-content">
      <a href="https://github.com/Leorodrigs" target="_blank">GitHub</a>
      <a
        href="https://drive.google.com/file/d/15YyNxSX_stxI6JXGGv-wfBlM0ciFJmcj/view?usp=sharing"
        target="_blank"
        >Currículo</a
      >
      <a
        href="https://www.linkedin.com/in/leonardo-rodrigues-558149248/"
        target="_blank"
        >LinkedIn</a
      >
    </div>
  </app-accordion>
</template>

<script>
export default {
  name: "AppPortfolio",
};
</script>

<style scoped>
.portfolio-content {
  text-align: center;
  display: flex;
  justify-content: center;
  gap: 30px;
}

@media (max-width: 480px) {
  .portfolio-content {  
    font-size: 50%;
}
}

.portfolio-content a {
  display: block;
  margin: 10px 0;
  color: blue;
  text-decoration: none;
}
</style>

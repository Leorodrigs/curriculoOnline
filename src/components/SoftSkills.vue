<template>
  <div class="soft-skills">
    <ul class="skills-list">
      <li v-for="(skill, index) in skills" :key="index">{{ skill }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "SoftSkills",
  data() {
    return {
      skills: [
        "Capacidade de Aprendizado",
        "Adaptabilidade",
        "Comunicação Eficaz",
        "Trabalho em Equipe",
        "Resolução de Problemas",
        "Atenção aos Detalhes",
        "Gestão de Tempo",
        "Receptividade a Feedback",
      ],
    };
  },
};
</script>

<style scoped>
.soft-skills {
  text-align: center;
}

.skills-list {
  list-style-type: disc;
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 50px;
  padding: 50;
  text-align: left;
}
</style>

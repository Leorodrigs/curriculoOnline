<template>
  <div class="HardSkills">
    <div class="icons">
      <img
        v-for="(skill, index) in skills"
        :key="index"
        :src="skill"
        alt="Skill Icon"
      />
    </div>
  </div>
</template>

<script>
export default {
  name: "HardSkills",
  data() {
    return {
      skills: [
        require("../assets/icons/css.svg"),
        require("../assets/icons/html.svg"),
        require("../assets/icons/javascript.svg"),
        require("../assets/icons/typescript.svg"),
        require("../assets/icons/angular.svg"),
        require("../assets/icons/react.svg"),
        require("../assets/icons/vuejs.svg"),
        require("../assets/icons/nodejs.svg"),
        require("../assets/icons/csharp.svg"),
        require("../assets/icons/dotnet.svg"),
        require("../assets/icons/django.svg"),
        require("../assets/icons/python.svg"),
      ],
    };
  },
};
</script>

<style scoped>
.HardSkills {
  display: flex;
  justify-content: center;
  align-items: center;
}

.icons {
  display: grid;
  grid-template-columns: repeat(6, 1fr);
  gap: 50px;
}

.icons img {
  width: 50px;
  height: 50px;
}
</style>

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

@media (max-width: 1024px) {
  .HardSkills{  
  display: block;
}
}

@media (max-width: 768px) {
  .HardSkills{  
  display: block;
}
}

@media (max-width: 480px) {
  .HardSkills{  
  display: block;
}
}

.icons {
  display: grid;
  grid-template-columns: repeat(6, 1fr);
  gap: 50px;
  margin-bottom: 2%;
}

@media (max-width: 1024px) {
  .icons {  
    margin-bottom: 2%;
    margin-left: 1%;
    gap: 10%     
}
}

@media (max-width: 768px) {
  .icons {  
    margin-bottom: 2%;
    margin-left: 5%;
    gap: 5% 
}
}

@media (max-width: 480px) {
  .icons {  
    margin-bottom: 5%;
    gap: 10%
}
}

.icons img {
  width: 50px;
  height: 50px;
}

@media (max-width: 768px) {
  .icons img {  
    width: 40px;
    height: 40px;
}
}

@media (max-width: 480px) {
  .icons img {  
    width: 32px;
    height: 32px;
}
}
</style>

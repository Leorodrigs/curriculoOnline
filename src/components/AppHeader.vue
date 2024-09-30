<template>
  <div class="header">
    <img :src="profilePic" alt="Foto de Perfil" class="profile-pic" />
    <div class="info">
      <h1>{{ name }}</h1>
      <p>{{ degree }}</p>
      <p>{{ location }}</p>
      <p>{{ phone }}</p>
      <p>{{ email }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "AppHeader",
  data() {
    return {
      profilePic: require("../assets/profile.png"),
      name: "Leonardo Rodrigues",
      degree: "Desenvolvedor Full-Stack Junior",
      location: "Porto Alegre - RS",
      phone: "(51) 9 8979-8998",
      email: "leorodrigues.job@gmail.com",
    };
  },
};
</script>

<style scoped>
.header {
  display: flex;
  align-items: center;
  justify-content: flex-start;
}

@media (max-width: 480px) {
  .header {  
    display: block;
    justify-content: center;
    text-align: center;
    margin-left: 5%;  
    font-size: 75%;  
}
}

.profile-pic {
  border-radius: 50%;
  width: 150px;
  height: 150px;
  margin-right: 20px;
}


.info h1 {
  font-size: 1.5em;
  margin: 0;
}


.info p {
  margin: 5px 0;
}


</style>

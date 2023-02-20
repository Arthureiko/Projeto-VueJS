<template>
  <div>
    <p v-if="!esta_trabalhando">Estou trabalhando no momento.</p>
    <p v-else>Estou em busca de novas oportunidades.</p>
    <p>Utilizo as seguintes tecnologias:</p>
    <ul>
      <li>Javascript</li>
      <li>PHP</li>
      <li>C++</li>
    </ul>
    <div>
      <button @click="showEmail">{{ textButton }}</button>
    </div>
    <p v-show="mostrar_email">Mandar email para: {{ email }}</p>
    <p>
      Para acessar meu portifólio
      <a v-bind:href="meu_link" target="_blank">basta clicar aqui</a>
    </p>
    <Picture />
  </div>
</template>

<script>
import Picture from "./Picture.vue";

export default {
  name: "Info",
  components: {
    Picture,
  },
  data() {
    return {
      esta_trabalhando: true,
      mostrar_email: false,
      email: "arthureiko29@gmail.com",
      meu_link: "https://google.com",
      textButton: "Mostrar email",
    };
  },
  methods: {
    showEmail() {
      this.mostrar_email = !this.mostrar_email;
      if (!this.mostrar_email) {
        this.textButton = "Mostrar email";
      } else {
        this.textButton = "Esconder email";
      }
    },
  },
};
</script>
<template>
  <div>
    <h1>Hellow</h1>
    <p v-for="(nomes, i) in nomes" :key="i">My name is: {{ nomes.name }}</p>
  </div>
</template>

<script>
export default {
  name: "FirstComponent",
  data() {
    return {
      nome: "Arthur",
    };
  },
  setup() {
    const nomes = [{ name: "Arthur" }, { name: "Eiko" }];
    return { nomes };
  },
};
</script>
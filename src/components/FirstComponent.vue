<template>
  <div>
    <h1>Hellow</h1>
    <p>My name is: {{ nome }}</p>
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
};
</script>
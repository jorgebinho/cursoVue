<template>
  <h2>Diretivas Condicionais</h2>

  <div v-show="showName">
    Nome: {{ firstName }} <br />
    Sobrenome: {{ lastName }}
  </div>

  <div v-if="accesLevel === 'adm'">Admin</div>
  <div v-else-if="accesLevel === 'mkt'">Marketing</div>
  <div v-else>User</div>
</template>

<script>
export default {
  data() {
    return {
      showName: true,
      firstName: "Jorge",
      lastName: "Santos",
      accesLevel: "user",
    };
  },
};
</script>

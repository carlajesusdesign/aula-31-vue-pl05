<template>
  <div>
    <h1>{{ cumprimento }}</h1>
  </div>
</template>

<script>
export default {
  name: 'Hello',
  props: {
    label: {
      type: String,
      required: true,
    },
  },
  computed: {
    cumprimento() {
      let curHour = new Date().getHours();
      let cumprimentoTxt;

      if (curHour < 12) {
        cumprimentoTxt = 'Bom dia';
      } else if (curHour < 18) {
        cumprimentoTxt = 'Boa tarde';
      } else {
        cumprimentoTxt = 'Boa noite';
      }
      return `${cumprimentoTxt} ${this.label}`;
    },
  },
};
</script>

<style scoped></style>

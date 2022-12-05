<template>
  <div>
    <h1>{{ inputValue }}</h1>
    <input v-model="inputValue" type="text" placeholder="Insira uma palavra" />
  </div>
</template>

<script>
export default {
  name: 'InputField',
  data() {
    return {
      inputValue: '',
    };
  },
};
</script>

<style scoped></style>

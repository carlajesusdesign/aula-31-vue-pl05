<template>
  <div>
    <h1>Bem-vindo {{ label }}</h1>
  </div>
</template>

<script>
export default {
  name: 'Welcome',
  props: {
    label: {
      type: String,
      required: true,
    },
  },
};
</script>

<style scoped></style>

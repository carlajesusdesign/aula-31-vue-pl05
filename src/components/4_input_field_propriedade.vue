<template>
  <div>
    <h1>{{ inputValueProps }}</h1>
    <input
      v-model="inputValueProps"
      type="text"
      placeholder="Insira uma palavra"
      v-blind:value="inputValueProps"
    />
  </div>
</template>

<script>
export default {
  name: 'InputFieldProps',
  props: {
    label: {
      type: String,
      required: true,
    },
  },
  data() {
    return {
      inputValueProps: this.label,
    };
  },
};
</script>

<style scoped></style>

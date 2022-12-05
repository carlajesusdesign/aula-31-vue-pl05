<script>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
// 1 passo - importar componentes
import Welcome from './components/1_welcome.vue';
import Hello from './components/2_hello.vue';
import InputField from './components/3_input_field.vue';
import InputFieldProps from './components/4_input_field_propriedade.vue';

// 2 passo - registar os componentes que importamos
export default {
  components: {
    Welcome,
    Hello,
    InputField,
    InputFieldProps,
  },
};
</script>

<template>
  <div>
    <a href="https://vitejs.dev" target="_blank">
      <img src="/vite.svg" class="logo" alt="Vite logo" />
    </a>
    <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>
  </div>
  <!-- 3 passo - aplicar a tag com a informação que precisamos, neste caso é o label e o componente registado -->
  <Welcome label="João" />
  <Hello label="João" />
  <InputField />
  <InputFieldProps label="" />
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>

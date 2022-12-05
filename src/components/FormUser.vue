<template>
  <form @submit.prevent="onSubmitHandler">
    <div>
      <label for="username">Username:</label>
      <input name="username" type="text" v-model="username">
    </div>
    <div>
      <label for="email">Email:</label>
      <input name="email" type="email" v-model="email">
    </div>
    <div>
      <label for="password">Password:</label>
      <input name="password" type="password" v-model="password">
    </div>
    <div>
      <label for="confirm_password">Confirm password:</label>
      <input name="confirm_password" type="password" v-model="confirm_password">
    </div>
    <div>
      <label for="senior_level">Level:</label>
      <select v-model="senior_level" name="senior_level" >
        <option value="junior">Junior</option>
        <option value="pleno">Pleno</option>
        <option value="senior">Senior</option>
      </select>
    </div>
    <div>
      <input v-model="accepted_terms" type="checkbox" name="accepted_terms">
      <label for="accepted_terms">Accept terms and conditions</label>
    </div>
    <button type="submit">Registar</button>
  </form>
</template>

<script>
  export default {
    data(){
      return {
        username: '',
        email: '',
        password : '',
        confirm_password : '',
        senior_level: '',
        accepted_terms: false
      }
    },
    methods: {
      onSubmitHandler(){
        // console.log(event)
        if(this.password !== this.confirm_password)
          alert('Passwords do not match')

        console.log(this.username, this.email, this.senior_level, this.accepted_terms)
      }
    }
  }
</script>

<style scoped></style>

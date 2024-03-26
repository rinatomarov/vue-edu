<template>
  <div class="form">
    <input type="password"  v-model="passWord" placeholder="Пароль">
    <p>{{passWord}}</p>
      <li v-if="passWord.length<=8">Пароль должен состоять из минимум 8 символов</li>
      <li v-if="!containsNumber.test(passWord)">Пароль должен включать хотя бы одну цифру</li>
    <input type="password" v-model="passWord2" placeholder="Повторите пароль">
    <span v-show="passWord!==passWord2">Пароли не идентичные</span>
  </div>
</template>

<script setup>
import {ref} from "vue";
const passWord = ref('')
const passWord2 = ref('')
const containsNumber = /\d+/
</script>

<style scoped>
.form {
  display: flex;
  flex-direction: column;
  border: 1px solid #282828;
  max-width: fit-content;
  margin: 40px;
  padding: 20px;
  border-radius: 12px;
  gap: 20px;
}
li  {
  color: red;
}
input{
  height: 40px;
  border-radius: 8px;
  padding-left: 28px;
}
</style>
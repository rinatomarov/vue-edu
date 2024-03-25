<template>
  <div class="form">
    <input type="password" id="pwd"  placeholder="Пароль">
    <ul><span> Пароль не подходит к критериям:</span>
      <li>Пароль должен состоять из минимум 8 символов</li>
      <li>Пароль должен включать хотя бы одну цифру</li>
    </ul>
    <label for="pwd-repeat">
      Repeat password
    </label>
    <input type="password" id="pwd-repeat"  placeholder="Пароль">
  </div>
</template>

<script setup>

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
ul  {
  color: red;
}
input{
  height: 40px;
  border-radius: 8px;
}
</style>
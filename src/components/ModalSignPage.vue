<template>
  <div class="overlay">
    <div class="modal">
      <div class="header">
        <!-- named slot -->
        <slot name="header"></slot>
      </div>
      <div class="body">
        <input type="text" v-model="login" placeholder="Введите логин">
        <input type="password" v-model="passWord" placeholder="Введите пароль">
      </div>
      <div class="footer">
        <slot name="footer"></slot>
      </div>
    </div>

  </div>
</template>

<script setup>
import {ref} from "vue";

const login = ref('')
const passWord = ref('')
</script>

<style scoped>
.overlay {
  position: fixed;
  width: 100vw;
  height: 100vh;
  background: rgba(0,0,0, .3);
  top: 0;
  left: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: auto;
  flex-direction: column;

}

.modal {
  max-width: 400px;
  width: 100%;
  background: white;
  border-radius: 12px;
}

.header, .footer, .body {
  min-height: 20px;
  padding: 20px;

}
.body {
  display: flex;
  flex-direction: column;
  gap: 20px;
}
</style>
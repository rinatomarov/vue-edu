<template>
  <div class="form">
    <input type="text" v-model="inputValue">
    <button @click="send">Отправить</button>
<!--    <span>{{ inputValue }}</span>-->
  </div>
</template>

<script>
import {ref, defineComponent} from "vue";

export default defineComponent({
  setup(_, {emit}) { // Получаем emit из контекста setup
    const inputValue = ref('');

    const send = () => {
      // Вызываем событие 'send' и передаем значение inputValue
      emit('send', inputValue.value);
    };

    return {
      inputValue,
      send
    };
  }
});
</script>

<style scoped>
.form {
  display: flex;
  border: 1px solid #282828;
  max-width: fit-content;
  margin: 40px;
  padding: 20px;
  border-radius: 12px;
  gap: 20px;
}
</style>

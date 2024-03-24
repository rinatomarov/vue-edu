<template>
  <div>
    <InputMailForm @send="updateMail"></InputMailForm>
    <div class="form">
      <h3>Введен почта {{ mailValue }} </h3>
    </div>
  </div>
</template>

<script>
import InputMailForm from "@/components/InputMailForm.vue";
import { ref } from "vue";

export default {
  components: {
    InputMailForm
  },
  setup() {
    const mailValue = ref(''); // Переменная для хранения значения почты

    const updateMail = (value) => {
      // Обновляем значение mailValue при получении события 'send' от InputMailForm.vue
      mailValue.value = value;
      console.log(mailValue.value); // Проверяем, обновилось ли значение mailValue
    };

    return {
      mailValue,
      updateMail
    };
  }
}
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

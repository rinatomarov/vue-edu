<template>
<!--    <Counter></Counter>-->
<!--    <Quotations></Quotations>-->
<!--    <Counter></Counter>-->
<!--    <p>Hello World</p>-->

<!--    <FirstDemo text="Нажми меня"></FirstDemo>-->
<!--    <FirstDemo text="Press me"></FirstDemo>-->
<!--    <FirstDemo text="Submit"></FirstDemo>-->

<!--    <AddImage></AddImage>-->

<!--  <SliderImage></SliderImage>-->

<!--    <AddCards></AddCards>-->
<!--  <InputMailForm></InputMailForm>-->
<!--  <PrintMail></PrintMail>-->
  <!--<PasswordValidation></PasswordValidation>-->
    <ModalSignPage>
      <template #header>
          <p>Прошу ввести ваши регистрационные данные:</p>
      </template>
      <template>
      </template>
      <template #footer>
        <button>Перейти в сайт</button>
      </template>
    </ModalSignPage>
  <h1>Login : {{login}}</h1>
  <h1>PassWord : {{passWord}}</h1>
</template>

<script setup>
// import FirstDemo from "@/components/FirstDemo.vue";
// import Counter from "@/components/Counter.vue";
// import Quotations from "@/components/icons/Quotations.vue";
import AddImage from "@/components/AddImage.vue";
import SliderImage from "@/components/SliderImage.vue";
import AddCards from "@/components/AddCards.vue";
// import PrintEmail from "@/components/InputMailForm.vue";
// import InputMailForm from "@/components/InputMailForm.vue";
import PrintMail from "@/components/PrintMail.vue";
import PasswordValidation from "@/components/PasswordValidation.vue";
import { computed, ref } from "vue";
import ModalSignPage from "@/components/ModalSignPage.vue";


</script>

<style>
p {
  color: red;
}
</style>
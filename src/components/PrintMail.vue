<template>
    <InputMailForm v-on:receiveMail="receiveMailEmit"></InputMailForm>
  <div class="form">
    <h3>Введен почта {{mail}}</h3>
  </div>
</template>

<script>
import InputMailForm from '@/components/InputMailForm.vue'
import { computed, ref } from "vue";
import {defineComponent} from "vue";
export default {
  components:{InputMailForm},
  data(){
    return {
      mail:''
    }
  },
  methods:{
    receiveMailEmit(mail){
      this.mail = mail
    }
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

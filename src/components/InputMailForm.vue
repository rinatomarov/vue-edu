<template>
  <div class="form">
    <input type="text" v-model="mail" placeholder="Прошу ввести вашу почту">
    <button v-on:click="send">Отправить</button>
<!--    <span>{{ mail }}</span>-->
  </div>
</template>

<script>
export default {
  data(){
    return {
      mail:'@gmail.com'
    }
  },
  methods:{
    send(){
      this.$emit('receiveMail',this.mail)
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

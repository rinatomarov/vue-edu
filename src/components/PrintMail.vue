<template>
  <InputMailForm :value="defaultMail"></InputMailForm>
  {{ defaultMail }}
  <div class="form">
    <h3></h3>
  </div>
</template>

<script>
import {ref} from "vue";
import InputMailForm from "@/components/InputMailForm.vue";
import {defineComponent} from "vue";

export default defineComponent({
  components: {InputMailForm}
})


const defaultMail = ref('John')
</script>

<style scoped>
.form{
  display: flex;
  border: 1px solid #282828;
  max-width: fit-content;
  margin: 40px;
  padding: 20px;
  border-radius: 12px;
  gap: 20px;
}
</style>
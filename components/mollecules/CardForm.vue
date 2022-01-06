<template>
  <div class="float-left pt-5 pb-8 px-14 bg-blue-200 rounded-xl" >
    <h1 class="text-xl font-bold text-center">Registration Form</h1>
    <InputText labelInput="Firstname" v-model="CardForm.fnameL"/>
    <InputText labelInput="Lastname" v-model="CardForm.lnameL"/>
    <InputRadio label="Man" name="gender" inputValue="Man" v-model="CardForm.genderL"/>
    <InputRadio label="Woman" name="gender" inputValue="Woman" v-model="CardForm.genderL"/>
    <InputText labelInput="Email" v-model="CardForm.emailL"/>
    <InputText labelInput="NumberPhone" v-model="CardForm.numberL"/>
    <InputText labelInput="Adress" v-model="CardForm.adressL"/>
    <InputText labelInput="PostalCode" v-model="CardForm.postalL"/>
    <Button @onClick="addData" labelButton="Click Me"/>
  </div>
</template>

<script>
import Button from "~/components/atoms/Button"
import InputRadio from "~/components/atoms/InputRadio"
import InputText from "~/components/atoms/InputText"
export default {
  components:{ 
    Button,
    InputRadio,
    InputText,
  },
  props:{
    CardForm:{
      type:Object,
      default:{}
    }
  },
  methods:{
    addData(){
      this.$emit("clickToButton")
    }
  }
}
</script>

<style>

</style>
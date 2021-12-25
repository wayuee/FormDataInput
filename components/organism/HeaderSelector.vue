<template>
  <div>
    <CardForm :card-form="CardForm" @clickToButton="addDataForm"/>
    <CardData :card-data="CardData" />
  </div>
</template>

<script>
import CardForm from "~/components/moleculles/CardForm"
import CardData from "~/components/moleculles/CardData"
export default {
  components:{
    CardForm,
    CardData,
  },
  props:{
    CardForm:{
      type:Object,
      default:{}
    },
    CardData:{
      type:Object,
      default:{}
    }
  },
  methods:{
    addDataForm(){
    this.$emit("clickButton")
    }
  }
}
</script>

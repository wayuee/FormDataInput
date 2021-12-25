<template>
  <div>
    <CardForm :card-form="CardForm" @clickToButton="addDataForm"/>
    <CardData :card-data="CardData" />
  </div>
</template>

<script>
import CardForm from "~/components/mollecules/CardForm"
import CardData from "~/components/mollecules/CardData"
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

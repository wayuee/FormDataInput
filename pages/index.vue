<template>
  <div>
    <HeaderSelector :card-form="CardForm" :card-data="CardData" @clickButton="addDataForm"/>
  </div>
</template>

<script>
import HeaderSelector from "~/components/organism/HeaderSelector"
export default {
  components: {
    HeaderSelector,
  },
  data() {
    return {
      CardForm: {
        fnameL: "",
        lnameL: "",
        genderL: "",
        genderL: "",
        emailL: "",
        numberL: "",
        adressL: "",
        postalL: "",
      },
      CardData: {
        fnameR: "",
        lnameR: "",
        genderR: "",
        emailR: "",
        numberR: "",
        adressR: "",
        postalR: "",
      },
    };
  },
  methods: {
    addDataForm() {
      // alert("hidup")
      // console.log(this.CardForm.fnameL)
      this.CardData.fnameR = this.CardForm.fnameL;
      this.CardData.lnameR = this.CardForm.lnameL;
      this.CardData.genderR = this.CardForm.genderL;
      this.CardData.genderR = this.CardForm.genderL;
      this.CardData.emailR = this.CardForm.emailL;
      this.CardData.numberR = this.CardForm.numberL;
      this.CardData.adressR = this.CardForm.adressL;
      this.CardData.postalR = this.CardForm.postalL;
    },
  },
};
</script>

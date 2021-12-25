<template>
  <label :for="labelInput" class="text-"
    >{{ labelInput }} : <br />
    <input
      type="text"
      class="w-full my-3 pr-96 py-2 border rounded-xl"
      :placeholder="labelInput"
      :value="inputValue"
      @input="inputData"
    />
    <br />
  </label>
</template>

<script>
export default {
  props: {
    labelInput: {
      type: String,
      default: "",
    },
    inputValue:{
      type:String,
      default:""
    },
  },
  methods:{
    inputData(e){
      this.$emit("input", e.target.value)
    }
  }
};
</script>

<style></style>

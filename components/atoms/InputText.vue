<template>
  <label :for="labelInput" class="pl-4 text-sm"
    >{{ labelInput }} : <br />
    <input
      type="text"
      class="w-full my-1.5 pr-72 py-2 pl-5 border rounded-xl"
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

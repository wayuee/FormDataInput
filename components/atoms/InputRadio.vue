<template>
  <label class="text-sm" :for="label">
    <input
      type="radio"
      :id="label"
      :name="name"
      :value="inputValue"
      @change="onChange"
      class="mb-3"
    />
    {{ label }} <br>
  </label>
</template>

<script>
export default {
  props: {
    label: {
      type: String,
      default: "",
    },
    name: {
      type: String,
      default: "",
    },
    inputValue:{
      type:String,
      default:""
    }
  },
  methods: {
    onChange(e) {
      this.$emit("input", this.inputValue);
    },
  },
};
</script>

<style></style>

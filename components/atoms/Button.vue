<template>
  <button @click="$emit('onClick')" class="float-right px-10 py-4 mt-3 text-white border rounded-xl bg-blue-500">
    {{ labelButton }}
  </button>
</template>

<script>
export default {
  props: {
    labelButton: {
      type: String,
      default: "",
    },
  },
};
</script>

<style></style>

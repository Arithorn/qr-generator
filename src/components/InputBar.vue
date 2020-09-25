<template>
  <div class="ui action input centered">
    <sui-label> URL </sui-label>
    <input v-model="url" :placeholder="msg" />
    <sui-button primary @click="onClick">Submit</sui-button>
  </div>
</template>

<script>
export default {
  name: "InputBar",
  data() {
    return {
      msg: "Enter Url",
      url: "",
    };
  },
  methods: {
    onClick: function() {
      this.$emit("onSubmit", this.url);
    },
  },
};
</script>

<style scoped></style>

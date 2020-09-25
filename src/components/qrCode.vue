<template>
  <div v-if="url !== ''">
    <sui-card class="centered">
      <sui-image :src="qrUrl" alt="qrtag" />
      <sui-card-content>
        <sui-card-header>
          {{ url }}
        </sui-card-header>
      </sui-card-content>
    </sui-card>
  </div>
</template>
<script>
export default {
  props: {
    url: String,
  },
  computed: {
    qrUrl: function() {
      return "https://qrtag.net/api/qr_12.svg?url=" + this.url;
    },
  },
};
</script>
//

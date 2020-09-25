<template>
  <div id="app">
    <sui-container class="center aligned">
      <sui-grid class="one column centered align">
        <sui-grid-column class="one column centered align">
          <sui-grid-row class="one column centered align">
            <sui-segment raised>
              <InputBar @onSubmit="onSubmit" class="align" />
              <QRCode :url="url" class="centered" />
            </sui-segment>
          </sui-grid-row>
        </sui-grid-column>
      </sui-grid>
    </sui-container>
  </div>
</template>

<script>
import InputBar from "./components/InputBar";
import QRCode from "./components/qrCode";
// import axios from "axios";

export default {
  name: "App",
  data() {
    return {
      url: "",
    };
  },
  components: {
    InputBar,
    QRCode,
  },
  methods: {
    onSubmit: function(url) {
      this.url = url;
    },
  },
};
</script>

<style scoped>
.align {
  text-align: center;
}
</style>

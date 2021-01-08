<template>
  <div id="app">
    <Homepage />
  </div>
</template>

<script>
import Homepage from "./components/Homepage";
export default {
  name: "App",
  components: {
    Homepage,
  },
};
</script>

<style>
@import url(https://db.onlinewebfonts.com/c/52b251ec7bb8689dfb2c5bb64dbba704?family=Mediator+Narrow+Web+Ultra+Light);
@font-face {
  font-family: "Mediator";
  src: url("//db.onlinewebfonts.com/t/52b251ec7bb8689dfb2c5bb64dbba704.eot");
  src: url("//db.onlinewebfonts.com/t/52b251ec7bb8689dfb2c5bb64dbba704.eot?#iefix")
      format("embedded-opentype"),
    url("//db.onlinewebfonts.com/t/52b251ec7bb8689dfb2c5bb64dbba704.woff2")
      format("woff2"),
    url("//db.onlinewebfonts.com/t/52b251ec7bb8689dfb2c5bb64dbba704.woff")
      format("woff"),
    url("//db.onlinewebfonts.com/t/52b251ec7bb8689dfb2c5bb64dbba704.ttf")
      format("truetype"),
    url("//db.onlinewebfonts.com/t/52b251ec7bb8689dfb2c5bb64dbba704.svg#Mediator Narrow Web Ultra Light")
      format("svg");
}
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
html,
body {
  font-size: 10px;
  font-family: Mediator, sans-serif;
  font-weight: 100;
}
body {
  margin: 0;
}
</style>

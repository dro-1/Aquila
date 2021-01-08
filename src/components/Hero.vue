<template>
  <div>
    <img :src="model" />
  </div>
</template>

<script>
import model from "./../assets/model.png";
export default {
  name: "Hero",
  data: () => ({
    model,
  }),
};
</script>

<style scoped lang="scss">
div {
  height: 350px;
  background: #cd2b66;
  width: 50%;
  margin: 0 auto;
  display: flex;
  justify-content: center;
  align-items: flex-end;
  box-shadow: -5px 5px 20px 8px rgba(0, 0, 0, 0.2);
  img {
    width: 100%;
    height: 100%;
  }
}
@media screen and (min-width: 680px) {
  div {
    height: 500px;
    img {
      width: initial;
      height: initial;
    }
  }
}
@media screen and (min-width: 1000px) {
  div {
    height: 550px;
  }
}
</style>

<template>
  <div>
    <img :src="model" />
  </div>
</template>

<script>
import model from "./../assets/model.png";
export default {
  name: "Hero",
  props: {
    msg: String,
  },
  data: () => ({
    model,
  }),
};
</script>

<style scoped lang="scss">
div {
  height: 500px;
  background: #cd2b66;
  width: 50%;
  margin: 0 auto;
  display: flex;
  justify-content: center;
  align-items: flex-end;
  box-shadow: -5px 5px 20px 8px rgba(0, 0, 0, 0.2);
  img {
    position: absolute;
  }
}
</style>

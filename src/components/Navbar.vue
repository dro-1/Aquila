<template>
  <nav>
    <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#">About</a></li>
      <li><img :src="model2" /></li>
      <li><a href="#">Gallery</a></li>
      <li><a href="#">Contact</a></li>
    </ul>
  </nav>
</template>

<script>
import model2 from "./../assets/model2.jpg";
export default {
  name: "Navbar",
  data() {
    return {
      model2,
    };
  },
};
</script>

<style lang="scss" scoped>
nav {
  width: 60%;
  margin: 4rem auto 0;
  ul {
    display: flex;
    justify-content: space-between;
    align-items: center;
    list-style-type: none;
    margin: 0;
    width: 100%;
    li {
      width: 15%;
      &:last-child {
        padding-left: 30px;
      }
      a {
        color: white;
        font-size: 22px;
        letter-spacing: 8px;
        text-decoration: none;
        text-transform: uppercase;
      }
      img {
        height: 100px;
        width: 100px;
        border-radius: 50%;
      }
    }
  }
}
</style>

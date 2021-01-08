<template>
  <div class="container">
    <Sidebar />
    <h1>{{ header }}</h1>
    <Hero />
    <Navbar />
  </div>
</template>

<script>
import Hero from "./Hero";
import Navbar from "./Navbar";
import Sidebar from "./Sidebar";
export default {
  name: "Homepage",
  components: {
    Hero,
    Navbar,
    Sidebar,
  },
  data: () => ({
    header: "Aquila Aveion",
  }),
};
</script>

<style lang="scss">
.container {
  position: relative;
  width: 100%;
  padding-bottom: 3rem;
  background: linear-gradient(
    to right,
    #bd0f4d 0%,
    #bd0f4d 50%,
    #cb2964 50%,
    #cb2964 100%
  );

  & > h1 {
    color: white;
    font-size: 35px;
    font-weight: 100;
    padding: 6rem 0 4rem;
    text-align: center;
    text-transform: uppercase;
    letter-spacing: 20px;
  }
}
</style>

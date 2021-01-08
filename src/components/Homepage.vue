<template>
  <div class="container">
    <Sidebar v-bind:links="links" />
    <h1 v-bind:header="header">{{ header }}</h1>
    <Hero />
    <Navbar />
  </div>
</template>

<script>
import Hero from "./Hero";
import Navbar from "./Navbar";
import Sidebar from "./Sidebar";
import axios from "axios";
export default {
  name: "Homepage",
  components: {
    Hero,
    Navbar,
    Sidebar,
  },
  data: () => ({
    header: "",
    links: {},
  }),
  created() {
    axios
      .get("https://hirng-x2021.glitch.me/api")
      .then((resp) => {
        console.log(resp.data);
        this.header = resp.data.name;
        const links = resp.data.social_media;
        this.links = {
          email: `mailto:${links.email}`,
          instagram: `https://www.instagram.com/${links.instagram}`,
          twitter: `https://www.twitter.com/${links.twitter}`,
          snapchat: `https://www.snapchat.com/add/${links.snapchat}`,
        };
      })
      .catch(console.log);
  },
};
</script>

<style lang="scss">
.container {
  position: relative;
  min-height: 100vh;
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

<template>
  <nav>
    <ul>
      <li>
        <a :href="links.instagram"><img :src="instagram"/></a>
      </li>
      <li>
        <a :href="links.twitter"><img :src="twitter"/></a>
      </li>
      <li>
        <a :href="links.snapchat"><img :src="snapchat"/></a>
      </li>
      <li>
        <a :href="links.email"><img :src="mail"/></a>
      </li>
    </ul>
  </nav>
</template>

<script>
import twitter from "./../assets/twitter.svg";
import mail from "./../assets/mail.svg";
import instagram from "./../assets/instagram.svg";
import snapchat from "./../assets/snapchat.svg";
export default {
  name: "Sidebar",
  props: {
    links: Object,
  },
  data() {
    return {
      twitter,
      mail,
      instagram,
      snapchat,
    };
  },
};
</script>

<style lang="scss" scoped>
nav {
  position: absolute;
  right: 0;
  top: 50%;
  transform: translateY(-50%);
  ul {
    list-style-type: none;
    display: flex;
    justify-content: space-between;
    flex-direction: column;
    height: 200px;
    padding-right: 2rem;
    li {
      height: 30px;
      width: 30px;
      a {
        height: 100%;
        width: 100%;
        img {
          height: 100%;
          width: 100%;
        }
      }
    }
  }
}
</style>

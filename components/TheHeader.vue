<template>
  <div class="theHeader">
    <svg
      class="menu"
      @click="openMenu"
      width="24px"
      height="24px"
      viewBox="0 0 24 24"
      version="1.1"
      xmlns="http://www.w3.org/2000/svg"
      xmlns:xlink="http://www.w3.org/1999/xlink">
      <title>menu</title>
      <g
        stroke="none"
        stroke-width="1"
        fill="none"
        fill-rule="evenodd"
        class="Icons">
        <g
          fill="currentColor"
          class="menu">
          <path
            d="M18,18 L6,18 C5.447,18 5,17.552 5,17 C5,16.448 5.447,16 6,16 L18,16 C18.553,16 19,16.448 19,17 C19,17.552 18.553,18 18,18 M18,13 L6,13 C5.447,13 5,12.552 5,12 C5,11.448 5.447,11 6,11 L18,11 C18.553,11 19,11.448 19,12 C19,12.552 18.553,13 18,13 M18,8 L6,8 C5.447,8 5,7.552 5,7 C5,6.448 5.447,6 6,6 L18,6 C18.553,6 19,6.448 19,7 C19,7.552 18.553,8 18,8"
            id="Fill-102"></path>
        </g>
      </g>
    </svg>
    <div
      class="menu-mobile"
      v-show="menu">
      <div>
        <nav class="menu-mobile-links">
          <nuxtLink
            to="/about"
            @click="openMenu">
            About
          </nuxtLink>
          <nuxtLink
            to="/skills"
            @click="openMenu">
            skills
          </nuxtLink>
          <nuxtLink
            to="/projects"
            @click="openMenu">
            Experience
          </nuxtLink>
        </nav>
      </div>
    </div>

    <div v-if="desktop">
      <nav class="menu-links">
        <nuxtLink to="/about"><Button :button-text="about"> </Button></nuxtLink>
        <nuxtLink to="/skills"
          ><Button :button-text="skills"> </Button
        ></nuxtLink>
        <nuxtLink to="/projects">
          <Button :button-text="projects"> </Button>
        </nuxtLink>
        <a @click="scrollFooter"><Button :button-text="contact"> </Button></a>
      </nav>
    </div>
  </div>
</template>

<script setup lang="ts">
  //Consts
  const about = "About";
  const skills = "skills";
  const projects = "experience";
  const contact = "contacts";
  const emit = defineEmits(["event"]);
  const menu = ref<boolean>(false);
  const desktop = false;

  //functions
  function scrollFooter() {
    emit("event");
  }

  function openMenu() {
    menu.value = !menu.value;
  }
</script>
<style scoped>
  .theHeader {
    background-color: #aab1c3;
    width: 100%;
    box-shadow: 0 0 5px 0 rgb(16 30 30 / 10%), 0 0 7px 0 rgb(16 30 30 / 15%),
      0 0 9px 0 rgb(16 30 30 / 10%);
    position: fixed;
    height: 72px;
    display: grid;
    grid-template-columns: 2rem auto 2rem;
  }

  a.nuxt-link {
    color: rgb(221, 221, 221);
  }
  .menu {
    grid-column: 2;
    display: flex;
    align-self: center;
  }
  .menu-mobile {
    height: 100%;
    width: 100%;
    background-color: #3c4770;
    position: fixed;
  }
  .menu-mobile-links {
    display: flex;
    justify-content: space-around;
    flex-direction: column;
    gap: 1rem;
    position: relative;
  }

  .menu-mobile-links a {
    cursor: pointer;
    color: white;
    text-decoration: none;
    font-size: 18px;
    font-family: "karla";
  }

  /*
 .name {
    display: flex;
    align-items: center;
    flex-direction: column;
  }

  .header-title {
    font-size: 1.3rem;
    margin: 1rem 0 0 0;
    font-family: "karla";
    padding: 12px;
    text-align: center;
  }

  .header-subtitle {
    font-size: 1rem;
    margin: 0 0 1rem 0;
    font-family: "spectral";
    font-weight: 400;
  }

  a.nuxt-link {
    color: black;
  }

  .router-link-active .linkButton {
    background-color: #3c4770;
  }
  .menu-links {
    display: flex;
    justify-content: space-around;
  }

    .menu a {
    cursor: pointer;
    text-decoration: underline;
  }
*/
</style>

<template id="footer">
  <nav class="contacts">
    <ul
      v-for="contact in contacts"
      :key="contact"
    >
      <li>
        <a :href="contact.link">{{ contact.site }}</a>
      </li>
    </ul>
  </nav>
</template>

<script setup lang="ts">
  const contacts = [
    { site: "GitHub", link: "https://github.com/notter-lesly" },
    { site: "Linkedin", link: "https://www.linkedin.com/in/leslynotter/" },
    {
      site: "Whatsapp",
      link: "https://api.whatsapp.com/send?phone=310627586099",
    },
  ];
</script>

<style>
  #footer {
    background-color: #3c4770;
    height: 15vh;
  }

  .contacts {
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    align-items: center;
    font-family: "spectral";
  }

  .contacts a {
    cursor: pointer;
    color: rgb(210, 210, 210);
  }
</style>

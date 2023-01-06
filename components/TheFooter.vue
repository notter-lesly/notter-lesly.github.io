<script setup lang="ts">
const contacts = [
  { site: 'GitHub', link: 'https://github.com/notter-lesly' },
  { site: 'Linkedin', link: 'https://www.linkedin.com/in/leslynotter/' },
  {
    site: 'Whatsapp',
    link: 'https://api.whatsapp.com/send?phone=310627586099',
  },
]
</script>

<template id="footer">
  <nav>
    <ul class="contacts">
      <li v-for="contact in contacts" :key="contact">
        <a :href="contact.link">{{ contact.site }}</a>
      </li>
    </ul>
  </nav>
</template>

<style scoped lang="scss">
#footer {
  background-image: url('../assets/footer.png');
  height: 15vh;

  ::after {
    border-top-right-radius: -10px;
  }

  .contacts {
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    align-items: center;
    font-family: '$text-font';
    z-index: 2;
    height: 100%;
  }

  .contacts a {
    cursor: pointer;
    color: rgb(210, 210, 210);
  }
}
</style>

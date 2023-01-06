<script setup lang="ts">
const aboutMe = [
  {
    value:
      'My name is Lesly Notter dos Anjos, I am a Swiss/Brazilian citizien living in the Netherlands since 2020.',
    key: 0,
  },
  {
    value: 'I am friendly and caring and you will love to meet me!',
    key: 1,
  },
  {
    value:
      'On professional side, I have a bachelor degree in information systems and 1 year of experience as a frontender.',
    key: 2,
  },
  {
    value:
      'The technology I work with is html, css, vue, nuxt, javascript and typescript.',
    key: 3,
  },
  {
    value:
      'My hoobies are arts of any kind: singing, playing the guitar, drawing, and of course games and puzzles.',
    key: 4,
  },
]
</script>

<template>
  <div id="about">
    <h1 class="sub-title">About Me</h1>
    <div class="flex">
      <ul class="about-text">
        <li v-for="phrases in aboutMe" :key="phrases.key">
          <p>{{ phrases.value }}</p>
        </li>
      </ul>
    </div>
  </div>
</template>

<style lang="scss" scoped>
#about {
  grid-column: 2/5;
  grid-row: 2;
  justify-content: center;
  color: white;

  @include for-tablet-landscape-up {
    grid-column: 3/6;
    grid-row: 3;
  }
}

.about-text {
  padding: 1rem 0;
  margin-bottom: 1rem;
}

.flex {
  display: flex;
  flex-direction: column;
  align-items: center;
  @include for-tablet-landscape-up {
    flex-direction: row;
    align-items: center;
    justify-content: space-evenly;
  }
}

.menu-decoration-left {
  width: 15rem;
  height: 5rem;
  position: absolute;
  border: 1px solid white;
  align-self: center;
  grid-row: 4;
  z-index: 1;
  border-left: none;
  border-radius: 20%;
  opacity: 0.5;
  transform: rotate(45deg);
}
.menu-decoration-right {
  width: 15rem;
  height: 5rem;
  position: absolute;
  border: 1px solid white;
  align-self: center;
  grid-column: 3/5;
  grid-row: 6;
  z-index: 1;
  border-left: none;
  border-radius: 20%;
  opacity: 0.5;
  transform: rotate(-45deg);
}
</style>

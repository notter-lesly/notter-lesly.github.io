<script setup lang="ts">
interface ButtonProps {
  buttonText: Project
}

const props = defineProps<ButtonProps>()
</script>

<template>
  <button class="linkButton">{{ buttonText }}</button>
</template>

<style scoped lang="scss">
.linkButton {
  background-color: #3c4770;
  border-radius: 20%;
  color: azure;
  border-color: #8a2be2;
  box-shadow: rgba(0, 0, 0, 0.15) 0px 15px 25px,
    rgba(0, 0, 0, 0.05) 0px 5px 10px;
  font-family: '$text-font';
  @include for-tablet-landscape-up {
    font-size: 18px;
  }
}
</style>

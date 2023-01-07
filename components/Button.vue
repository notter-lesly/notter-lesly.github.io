<script setup lang="ts">
interface ButtonProps {
  buttonText: string
}
const props = defineProps<ButtonProps>()
</script>

<template>
  <button class="linkButton">{{ buttonText }}</button>
</template>

<style scoped lang="scss">
.linkButton {
  font-family: $text-font;
  background-color: $background;
  border-color: $border;
  border-radius: 20%;
  color: azure;
  box-shadow: rgba(0, 0, 0, 0.15) 0px 15px 25px,
    rgba(0, 0, 0, 0.05) 0px 5px 10px;

  @include for-tablet-landscape-up {
    font-size: 14px;
  }
}
</style>

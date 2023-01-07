<script setup lang="ts">
interface MeasureProps {
  skillMeasure: string
}

const props = defineProps<MeasureProps>()

const measureBar = ref(props.skillMeasure)
</script>

<template>
  <div id="measure">
    <div class="skill-fill" v-bind:style="{ width: measureBar }"></div>
  </div>
</template>

<style scoped lang="scss">
#measure {
  height: 1rem;
  background-color: #aab1c3;
  border: 1px solid rgb(134, 39, 155);
  width: 8rem;
}

.skill-fill {
  background-color: $background;
  height: 100%;
}
</style>

<template>
<div id="measure">
<div class="triangle" v-bind:style="{borderLeft: measureBar}">
</div>
</div>
</template>


<script setup lang="ts">

interface MeasureProps{

skillMeasure: Project
}

const props= defineProps<MeasureProps>()

const measureBar = ref(props.skillMeasure)


</script>

<style scoped>

#measure{
width: 300px;
height: 1rem;    
background-color: #AAB1C3;
border: 1px solid black;
position: relative;
}
.triangle {
  width: 0;
  height: 0;
  border: 5px solid transparent;
  border-top: 10px solid #3C4770;
  border-bottom: 0;
}


</style>
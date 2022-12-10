<template>
    <div id="measure">
        <div class="skill-fill" v-bind:style="{width: measureBar}">
        </div>
    </div>
</template>


<script setup lang="ts">

interface MeasureProps{
    skillMeasure: string
}

const props = defineProps<MeasureProps>()

const measureBar = ref(props.skillMeasure)


</script>

<style scoped>

#measure{
height: 1rem;    
background-color: #AAB1C3;
border: 1px solid black;
width: 8rem;
}

.skill-fill{
    background-color: #3C4770;
    height: 100%;
}


</style>
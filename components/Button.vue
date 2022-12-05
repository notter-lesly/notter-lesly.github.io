<template>

<button class="linkButton"> {{ buttonText}}</button>

</template>

<script setup lang="ts">

export interface Props {
    buttonText: string

}

const props =  withDefaults(defineProps<Props>(), {
    buttonText: ''
})
</script>

<style>

.linkButton{

background-color: #BE8199;
border-radius: 20%;
color:azure;
border-color:blueviolet;
box-shadow: rgba(0, 0, 0, 0.15) 0px 15px 25px, rgba(0, 0, 0, 0.05) 0px 5px 10px;
}


</style>
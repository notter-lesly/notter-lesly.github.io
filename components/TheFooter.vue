<template id="TheFooter">
    <nav class="contacts">
        <ul v-for="contact in contacts" :key="contact" >
            <li><a :href="contact.link">{{contact.site}}</a></li>
        </ul>
    </nav>
</template>

<script setup>

const contacts = [
{'site':'GitHub', 'link': 'https://github.com/notter-lesly'},
{'site':'Linkedin', 'link':'https://www.linkedin.com/in/leslynotter/'},
{'site':'Whatsapp', 'link':'https://api.whatsapp.com/send?phone=310627586099'}
]


</script>

<style>
.contacts{
    display: flex;
    flex-direction: row;
    justify-content: space-around;
}

.contacts a{
cursor:pointer,

}

</style>
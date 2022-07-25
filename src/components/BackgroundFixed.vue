<template>
    <section class="background-cover background-fixed background-center w-100 h-70vh" v-bind:style="{'background-image': 'url(' + background + ')'}">

    </section>
</template>

<script>
    export default {
        name: 'BackgroundFixed',
        props: {
            background: String
        }
    }
</script>
<script setup>
const logo = {
    src: "images/client-logos.png",
    alt: "client logos",
    class : "img-fluid"
}
</script>

<template>
    <div class="client-logos my-5">
        <div class="container text-center">
            <p>These Company waiting for you!</p>
            <img v-bind="logo">
        </div>
    </div>
</template>
<style scoped>

</style>
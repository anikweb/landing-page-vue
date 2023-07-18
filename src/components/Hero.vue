<script setup>

const header = {
    title: "Mobile App Landing Page Template",
    subtitle: "The one and only solution for any kind of mobila app landing needs. Just change the screenshots and texts and you are good to go. ",
    heroImage: {
        src: "../../public/images/iphonex.png",
        alt: "phone",
        class: "img-fluid"
    }
    

}
</script>
<template>
    <header class="bg-gradient" id="home">
        <div class="container mt-5">
            <h1>{{ title }}</h1>
            <p class="tagline"></p>
        </div>
        <div class="img-holder mt-3"><img v-bind="header.heroImage"></div>
    </header>
</template>

<style>

header {
    padding: 100px 0 0;
    text-align: center;
    color: #FFF;
}

.bg-gradient {
    background-image: -moz-linear-gradient( 135deg, rgba(60, 8, 118, 0.8) 0%, rgba(250, 0, 118, 0.8) 100%);
    background-image: -webkit-linear-gradient( 135deg, rgba(60, 8, 118, 0.8) 0%, rgba(250, 0, 118, 0.8) 100%);
    background-image: -ms-linear-gradient( 135deg, rgba(60, 8, 118, 0.8) 0%, rgba(250, 0, 118, 0.8) 100%);
    background-image: linear-gradient( 135deg, rgba(60, 8, 118, 0.8) 0%, rgba(250, 0, 118, 0.8) 100%);
}

.tagline {
    font-size: 23px;
    font-weight: 300;
    color: #ffb8f6;
    max-width: 800px;
    margin: 0 auto;
}

.img-holder {
    height: 0;
    padding-bottom: 33%;
    overflow: hidden;
}

@media (max-width:1200px) {
    .img-holder {
        padding-bottom: 50%;
    }
}

@media (max-width:767px) {
    .tagline {
        font-size: 17px;
    }
    .img-holder {
        padding-bottom: 100%;
    }
}
</style>
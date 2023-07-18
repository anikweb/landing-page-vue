<script setup>
const imageGallery = {
    subtitle: 'GALLERY',
    title: 'App Screenshots',
    images: [
        {src: 'images/screen1.jpg', alt : 'image'},
        {src: 'images/screen2.jpg', alt : 'image'},
        {src: 'images/screen3.jpg', alt : 'image'},
        {src: 'images/screen4.jpg', alt : 'image'},        
        {src: 'images/screen5.jpg', alt : 'image'},       
        {src: 'images/screen6.jpg', alt : 'image'}        
        
    ]
}
</script>

<template>
     <div class="section light-bg" id="gallery">
        <div class="container">
            <div class="section-title">
                <small>{{ imageGallery.subtitle }}</small>
                <h3>{{ imageGallery.title }}</h3>
            </div>
            <div class="img-gallery owl-carousel owl-theme">
                <img v-for="(image, index) in imageGallery.images" :key="index" v-bind="image" />
            </div>
        </div>
    </div>
</template>

<style>
.img-gallery .owl-item {
    box-shadow: 0px 9px 32px 0px rgba(0, 0, 0, 0.07);
    transform: scale(0.8);
    transition: all 0.3s ease-in;
}

.img-gallery .owl-item.center {
    transform: scale(1);
}
</style>
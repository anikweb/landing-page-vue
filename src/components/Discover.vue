<script setup>
const discover = {
    title: 'Discover our App',
    summary :'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Obcaecati vel exercitationem eveniet vero maxime ratione ',
    icon: 'ti-mobile',
    image: {
        src: "images/perspective.png",
        alt: "perspective phone",
        class: "img-fluid"
    }
    
    
}
</script>

<template>
    <div class="section">
            <div class="container">
                <div class="row">
                    <div class="col-lg-6 offset-lg-6">
                        <div class="box-icon"><span :class="discover.icon" class=" gradient-fill ti-3x"></span></div>
                        <h2>{{ discover.title }}</h2>
                        <p class="mb-4">{{ discover.summary }}</p>
                        <a href="#" class="btn btn-primary">Read more</a>
                    </div>
                </div>
                <div class="perspective-phone">
                    <img v-bind="discover.image" />
                </div>
            </div>
        </div>    
</template>

<style scoped>

</style>
<script setup>
const contactInfo = {
    address : '1485 Pacific St, Brooklyn, NY 11216 USA',
    email : 'support@mobileapp.com',
    phone: '518-3636-2800',
    socials: [
        { 'platform': 'Facebook', icon: 'ti-facebook', url: 'https://www.facebook.com/'},
        { 'platform': 'Twitter', icon: 'ti-twitter-alt', url: 'https://www.twitter.com/'},
        { 'platform': 'Instagram', icon: 'ti-instagram', url: 'https://www.instagram.com/'},
    ]
}
</script>
<template>
    <div class="light-bg py-5" id="contact">
        <div class="container">
            <div class="row">
                <div class="col-lg-6 text-center text-lg-left">
                    <p class="mb-2"> <span class="ti-location-pin mr-2">{{ contactInfo.address }}</span> </p>
                    <div class=" d-block d-sm-inline-block">
                        <p class="mb-2">
                            <span class="ti-email mr-2"></span> <a class="mr-4" :href="'mailto:'+contactInfo.email">{{ contactInfo.email }}</a>
                        </p>
                    </div>
                    <div class="d-block d-sm-inline-block">
                        <p class="mb-0">
                            <span class="ti-headphone-alt mr-2"></span> <a :href="'tel:'+contactInfo.phone">{{ contactInfo.phone }}</a>
                        </p>
                    </div>
                </div>
                <div class="col-lg-6">
                    <div class="social-icons">
                        <a  v-for="(platform, index) in contactInfo.socials" :key="index" :title="platform.platform" target="_blank" :href="platform.url"><span :class="platform.icon"></span></a>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
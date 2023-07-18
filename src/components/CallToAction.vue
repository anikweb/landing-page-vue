<script setup>
const callToAction = {
    title: 'Download Anywhere',
    summary: 'Available for all major mobile and desktop platforms. Rapidiously visualize optimal ROI rather than enterprise-wide methods of empowerment.',
    warning : '*Works on iOS 10.0.5+, Android Kitkat and above. ',
    platforms: [
        {
            name: 'Play Store',
            link: 'https://play.google.com/store/search?q=ostad&c=apps',
            image: {
                src: 'images/playicon.png',
                alt: 'play store',
            }
        },
        {
            name: 'App Store',
            link: 'https://apps.apple.com/app/id6446163017',
            image: {
                src: 'images/appleicon.png',
                alt: 'play store',
            }
        }
    ]
}
</script>
<template>
    <div class="section bg-gradient">
        <div class="container">
            <div class="call-to-action">

                <div class="box-icon"><span class="ti-mobile gradient-fill ti-3x"></span></div>
                <h2>{{ callToAction.title }}</h2>
                <p class="tagline">{{ callToAction.summary }}</p>
                <div class="my-4">
                    <a v-for="(platform, index) in callToAction.platforms" :key="index" :href="platform.link" class="btn btn-light">
                        <img v-bind="platform.image" /> {{ platform.name }}
                    </a>
                </div>
                <p class="text-primary"><small><i>{{ callToAction.warning }}</i></small></p>
            </div>
        </div>
    </div>
</template>
<style>

.call-to-action {
    text-align: center;
    color: #FFF;
    margin: 3rem 0;
}

.call-to-action .box-icon {
    margin-left: auto;
    margin-right: auto;
    border-radius: 5px;
    transform: scale(0.85);
    margin-bottom: 2.5rem;
}

.call-to-action h2 {
    color: #FFF;
}

.call-to-action .tagline {
    font-size: 16px;
    font-weight: 300;
    color: #ffb8f6;
    max-width: 650px;
    margin: 0 auto;
}

.btn-light img {
    margin-right: 0.4rem;
    vertical-align: text-bottom;
}


/*  FOOTER
----------------------*/

.social-icons {
    text-align: right;
}

.social-icons a {
    background-color: #FFF;
    box-shadow: 0px 0px 21px 0px rgba(0, 0, 0, 0.05);
    width: 50px;
    height: 50px;
    display: inline-block;
    text-align: center;
    line-height: 50px;
    margin: 0 0.3rem;
    border-radius: 5px;
    color: #f4c9e2;
    transition: all 0.3s ease;
}

.social-icons a:hover {
    text-decoration: none;
    color: #e38cb7;
}

@media (max-width:991px) {
    .social-icons {
        text-align: center;
        margin-top: 2rem;
    }
}
</style>
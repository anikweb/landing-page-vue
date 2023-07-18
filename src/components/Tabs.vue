<script setup>
const tabs = {
    title : "Do more with our app",
    summary: "FEATURES",
    links: ['ABOUT US'],
    items: [
        {
            id : 'ABOUT US',
            title: 'What we are?',
            subtitle: '',
            summary: 'Ostad is a skill development platform focusing on live learning. We have 30,000+ users on our platform and 4500+ learners who graduated and are still learning in Ostad.We provide skill development opportunities to university students, job holders, job seekers, and freelancers who want to learn or develop skills from the best instructors. Develop your skill with the best industry experts through live learning, task-based curriculum, and track your progress through our progress tracking dashboard. Get all the resources easily and get access to one of the richest talentpools.Trade licence number- 164424',
            img: {
                src:"images/graphic.png",
                alt:"graphic"
            }
        },

    ]
        
}
</script>

<template>
    <div class="section light-bg">
        <div class="container">
            <div class="section-title">
                <small>{{ tabs.summary }}</small>
                <h3>{{ tabs.title }}</h3>
            </div>

            <ul class="nav nav-tabs nav-justified" role="tablist">
                <li class="nav-item" v-for="(link, index) in tabs.links" :key="index">
                    <a  class="nav-link " :class="0 == index ? 'active' : ''"  data-toggle="tab" :href="`#${link.trim().toLocaleLowerCase().split(' ').join('')}`">{{ link }}</a>
                </li>
            </ul>
            <div class="tab-content">
                <div v-for="(item, index) in tabs.items" :key="item.id" class="tab-pane fade " :class="0 == index ? 'show active' : ''" :id="item.id">
                    <div class="d-flex flex-column flex-lg-row">
                        <img  v-bind="item.img" class="img-fluid about-image rounded align-self-start mr-lg-5 mb-5 mb-lg-0">
                        <div>
                            <h2>{{ item.title }}</h2>
                            <p class="lead">{{ item.subtitle }}</p>
                            <p>{{ item.summary }}</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style>

.tab-content {
    border-bottom-right-radius: 3px;
    border-bottom-left-radius: 3px;
    background-color: #FFF;
    box-shadow: 0px 5px 7px 0px rgba(0, 0, 0, 0.04);
    padding: 3rem;
}

@media (max-width:992px) {
    .tab-content {
        padding: 1.5rem;
    }
    
  
}


/* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 600px) {
    .about-image{
        width: 100%;
    }
}

/* Small devices (portrait tablets and large phones, 600px and up) */
@media only screen and (min-width: 600px) {
     .about-image{
        width: 100%;
    }
}

/* Medium devices (landscape tablets, 768px and up) */
@media only screen and (min-width: 768px) {
     .about-image{
        width: 100%;
    }
}

/* Large devices (laptops/desktops, 992px and up) */
@media only screen and (min-width: 992px) {
     .about-image{
        max-width: 30%;
    }
}

/* Extra large devices (large laptops and desktops, 1200px and up) */
@media only screen and (min-width: 1200px) {
     .about-image{
        max-width: 30%;
    }
}

.tab-content p {
    line-height: 1.8;
}

.tab-content h2 {
    margin-bottom: 0.5rem;
}

.nav-tabs {
    border-bottom: 0;
}

.nav-tabs .nav-item .nav-link,
.nav-tabs .nav-link:focus,
.nav-tabs .nav-link:hover {
    padding: 1rem 1rem;
    border-color: #faf6fb #faf6fb #FFF;
    font-size: 19px;
    color: #b5a4c8;
    background: #f5eff7;
}

.nav-tabs .nav-link.active {
    background: #FFF;
    border-top-width: 3px;
    border-color: #ce75b4 #faf6fb #FFF;
    color: #633991;
}
</style>
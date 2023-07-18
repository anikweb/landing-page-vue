<script setup>

const testimonials = {
    subtitle: 'TESTIMONIALS',
    title: 'What our Customers Says',
    items: [
        {
            quote: 'Uniquely streamline highly efficient scenarios and 24/7 initiatives. Conveniently embrace multifunctional ideas through proactive customer service. Distinctively conceptualize 2.0 intellectual capital via user-centric partnerships.',
            name: 'Crystal Gordon',
            designation: 'United States',
            image: {
                src: "images/client.png",
                alt: "client",
                class: "client-img"
            }
            
        },
        {
            quote: 'Uniquely streamline highly efficient scenarios and 24/7 initiatives. Conveniently embrace multifunctional ideas through proactive customer service. Distinctively conceptualize 2.0 intellectual capital via user-centric partnerships.',
            name: 'Crystal Gordon',
            designation: 'United States',
            image: {
                src: "images/client.png",
                alt: "client",
                class: "client-img"
            }
            
        },
        {
            quote: 'Uniquely streamline highly efficient scenarios and 24/7 initiatives. Conveniently embrace multifunctional ideas through proactive customer service. Distinctively conceptualize 2.0 intellectual capital via user-centric partnerships.',
            name: 'Crystal Gordon',
            designation: 'United States',
            image: {
                src: "images/client.png",
                alt: "client",
                class: "client-img"
            }
            
        },
        {
            quote: 'Uniquely streamline highly efficient scenarios and 24/7 initiatives. Conveniently embrace multifunctional ideas through proactive customer service. Distinctively conceptualize 2.0 intellectual capital via user-centric partnerships.',
            name: 'Crystal Gordon',
            designation: 'United States',
            image: {
                src: "images/client.png",
                alt: "client",
                class: "client-img"
            }
            
        },
    ]
}
</script>

<template>
    <div class="section">
    <div class="container">
        <div class="section-title">
            <small>{{ testimonials.subtitle }}</small>
            <h3>{{ testimonials.title }}</h3>
        </div>

        <div class="testimonials owl-carousel">
            <div v-for="(item , index) in testimonials.items" :key="index" class="testimonials-single">
                <img v-bind="item.image"/>
                <blockquote class="blockquote">{{ item.quote }}</blockquote>
                <h5 class="mt-4 mb-2">{{ item.name }}</h5>
                <p class="text-primary">{{ item.designation }}</p>
            </div>
        </div>

    </div>

    </div>    
</template>

<style>

.owl-carousel .owl-item img.client-img {
    width: 110px;
    margin: 30px auto;
    border-radius: 50%;
    box-shadow: 0px 9px 32px 0px rgba(0, 0, 0, 0.07);
}

.testimonials-single {
    text-align: center;
    max-width: 80%;
    margin: 0 auto;
}

.blockquote {
    color: #7a767a;
    font-weight: 300;
}

.owl-next.disabled,
.owl-prev.disabled {
    opacity: 0.5;
}

.owl-prev,
.owl-next {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
}

.owl-prev {
    left: 0;
}

.owl-next {
    right: 0;
}

.owl-theme .owl-nav.disabled+.owl-dots {
    margin-top: 60px;
}

.owl-theme .owl-dots .owl-dot span {
    background: #e7d9eb;
    width: 35px;
    height: 8px;
    border-radius: 10px;
    transition: all 0.3s ease-in;
}

.owl-theme .owl-dots .owl-dot:hover span {
    background: #ff487e;
}

.owl-theme .owl-dots .owl-dot.active span {
    background: #ff487e;
    box-shadow: 0px 9px 32px 0px rgba(0, 0, 0, 0.07);
}
</style>
<script setup>

const features = {
    title: "Features you love",
    subtitle: "HIGHLIGHTS",
    items: [
        {
            title: 'Simple',
            summary: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer rutrum, urna eu pellentesque",
            icon: 'ti-face-smile'
        },
         {
            title: 'Customize',
            summary: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer rutrum, urna eu pellentesque",
            icon: 'ti-settings'
        },
         {
            title: 'Secure',
            summary: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer rutrum, urna eu pellentesque",
            icon: 'ti-lock '
        }       
    ]
    
}

</script>

<template>
    <div class="section light-bg" id="features">
        <div class="container">
            <div class="section-title">
                <small>{{ features.subtitle }}</small>
                <h3>{{ features.title }}</h3>
            </div>
            <div class="row">
                <div v-for="(item, index) in features.items" :key="index" class="col-12 col-lg-4">
                    <div class="card features">
                        <div class="card-body">
                            <div class="media">
                                <span class=" gradient-fill ti-3x mr-3" :class="item.icon"></span>
                                <div class="media-body">
                                    <h4 class="card-title">{{ item.title  }}</h4>
                                    <p class="card-text">{{ item.summary }}</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style>

.gradient-fill:before {
    color: #fc73b4;
    background: -moz-linear-gradient(top, #9477b4 0%, #fc73b4 100%);
    background: -webkit-linear-gradient(top, #9477b4 0%, #fc73b4 100%);
    background: linear-gradient(to bottom, #9477b4 0%, #fc73b4 100%);
    -webkit-background-clip: text;
    background-clip: text;
    -webkit-text-fill-color: transparent;
}

.card.features {
    border: 0;
    border-radius: 3px;
    box-shadow: 0px 5px 7px 0px rgba(0, 0, 0, 0.04);
    transition: all 0.3s ease;
}

@media (max-width:991px) {
    .card.features {
        margin-bottom: 2rem;
    }
    [class^="col-"]:last-child .card.features {
        margin-bottom: 0;
    }
}

.card.features:before {
    content: "";
    position: absolute;
    width: 3px;
    color: #fc73b4;
    background: -moz-linear-gradient(top, #9477b4 0%, #fc73b4 100%);
    background: -webkit-linear-gradient(top, #9477b4 0%, #fc73b4 100%);
    background: linear-gradient(to bottom, #9477b4 0%, #fc73b4 100%);
    top: 0;
    bottom: 0;
    left: 0;
}

.card-text {
    font-size: 14px;
}

.card.features:hover {
    transform: translateY(-3px);
    -moz-box-shadow: 0px 5px 30px 0px rgba(0, 0, 0, 0.08);
    -webkit-box-shadow: 0px 5px 30px 0px rgba(0, 0, 0, 0.08);
    box-shadow: 0px 5px 30px 0px rgba(0, 0, 0, 0.08);
}

.box-icon {
    box-shadow: 0px 0px 43px 0px rgba(0, 0, 0, 0.14);
    padding: 10px;
    width: 70px;
    border-radius: 3px;
    margin-bottom: 1.5rem;
    background-color: #FFF;
}

.circle-icon {
    box-shadow: 0px 9px 32px 0px rgba(0, 0, 0, 0.07);
    padding: 10px;
    width: 100px;
    height: 100px;
    border-radius: 50%;
    margin-bottom: 1.5rem;
    background-color: #FFF;
    color: #f5378e;
    font-size: 48px;
    text-align: center;
    line-height: 80px;
    font-weight: 300;
    transition: all 0.3s ease;
}

@media (max-width:992px) {
    .circle-icon {
        width: 70px;
        height: 70px;
        font-size: 28px;
        line-height: 50px;
    }
}

.ui-steps li:hover .circle-icon {
    background-image: -moz-linear-gradient( 122deg, #e6388e 0%, #fb378e 100%);
    background-image: -webkit-linear-gradient( 122deg, #e6388e 0%, #fb378e 100%);
    background-image: -ms-linear-gradient( 122deg, #e6388e 0%, #fb378e 100%);
    background-image: linear-gradient( 122deg, #e6388e 0%, #fb378e 100%);
    box-shadow: 0px 9px 32px 0px rgba(0, 0, 0, 0.09);
    color: #FFF;
}

.ui-steps li {
    padding: 15px 0;
}

.ui-steps li:not(:last-child) {
    border-bottom: 1px solid #f8e3f0;
}

.perspective-phone {
    position: relative;
    z-index: -1;
}

@media (min-width:992px) {
    .perspective-phone {
        margin-top: -150px;
    }
}

</style>
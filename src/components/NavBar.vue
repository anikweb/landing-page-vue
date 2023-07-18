<script setup>
const navLinks = ['HOME', 'FEATURES', 'GALLERY', 'PRICING', 'CONTACT']
const logo = {
    src: "images/logo.png",
    class: "img-fluid",
    alt: "logo"
}
</script>

<template>
    <div class="nav-menu fixed-top">
        <div class="container">
            <div class="row">
                <div class="col-md-12">
                    <nav class="navbar navbar-dark navbar-expand-lg">
                        <a class="navbar-brand" href="/">
                            <img v-bind="logo" />
                        </a>
                            <!-- <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbar" aria-controls="navbar" aria-expanded="false" aria-label="Toggle navigation"> <span class="navbar-toggler-icon"></span> </button> -->
                        <div class="collapse navbar-collapse" id="navbar">
                            <ul class="navbar-nav ml-auto">
                                <li v-for="(navLink, index) in navLinks" :key="index"  class="nav-item"> 
                                    <a class="nav-link" :class="index == 0 ? 'active' : ''"  :href="`#${navLink.toLowerCase()}`"> 
                                    <span v-show="index ==0" class="sr-only">(current)</span> {{ navLink }}</a> 
                                </li>
                                <li class="nav-item"><a href="#" class="btn btn-outline-light my-3 my-sm-0 ml-lg-3">Download</a></li>
                            </ul>
                        </div>
                    </nav>
                </div>
            </div>
        </div>
    </div>
</template>

<style>

.nav-menu {
    padding: 1rem 0;
    transition: all 0.3s ease;
}

.nav-menu.is-scrolling,
.nav-menu.menu-is-open {
    background-color: rgb(74, 13, 143);
    background: -moz-linear-gradient(135deg, rgb(74, 13, 143) 0%, rgb(250, 42, 143) 100%);
    background: -webkit-linear-gradient(135deg, rgb(74, 13, 143) 0%, rgb(250, 42, 143) 100%);
    background: linear-gradient(135deg, rgb(74, 13, 143) 0%, rgb(250, 42, 143) 100%);
    -webkit-box-shadow: 0px 5px 23px 0px rgba(0, 0, 0, 0.1);
    -moz-box-shadow: 0px 5px 23px 0px rgba(0, 0, 0, 0.1);
    box-shadow: 0px 5px 23px 0px rgba(0, 0, 0, 0.1);
}

.nav-menu.is-scrolling {
    padding: 0;
}

.navbar-nav .nav-link {
    position: relative;
}

@media (min-width: 992px) {
    .navbar-expand-lg .navbar-nav .nav-link {
        padding-right: 1rem;
        padding-left: 1rem;
        font-size: 14px;
    }
    .navbar-nav>.nav-item>.nav-link.active:after {
        content: "";
        border-bottom: 2px solid #cd99d4;
        left: 1rem;
        right: 1rem;
        bottom: 5px;
        height: 1px;
        position: absolute;
    }
}

@media (max-width:991px) {
    .navbar-nav.is-scrolling {
        padding-bottom: 1rem;
    }
    .navbar-nav .nav-item {
        text-align: center;
    }
}
</style>
<script setup>
const data = {
    img: {
        src: "images/iphonex.png",
        alt: "iphone",
        class: 'img-fluid'
    },
    items: [
        {
            step: '1',
            title: 'Create an Account',
            summary: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer rutrum, urna eu pellentesque pretium obcaecati vel exercitationem '
        },
        {
            step: '2',
            title: 'Share with friends',
            summary: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer rutrum, urna eu pellentesque pretium obcaecati vel exercitationem eveniet'
        },
        {
            step: '3',
            title: 'Enjoy your life',
            summary: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer rutrum, urna eu pellentesque pretium obcaecati vel exercitationem'
        },
    ]
}
</script>

<template>
     <div class="section light-bg">
              <div class="container">
                  <div class="row">
                      <div class="col-md-8 d-flex align-items-center">
                          <ul class="list-unstyled ui-steps">
                              <li v-for="(item, index) in data.items" :key="index" class="media">
                                  <div class="circle-icon mr-4">{{ item.step }}</div>
                                  <div class="media-body">
                                      <h5>{{ item.title }}</h5>
                                      <p>{{ item.summary }}</p>
                                  </div>
                              </li>
                          </ul>
                      </div>
                      <div class="col-md-4">
                          <img v-bind="data.img">
                      </div>

                  </div>

              </div>

          </div>
</template>

<style scoped>

</style>
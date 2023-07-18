<script setup>
const launchPhone = {
    title: "DATA SCIENCE",
    summary : 'Ostad-এ দেশের সবচেয়ে বড় ডাটা সায়েন্স cohort কে সাজানো হয়েছে একদম বিগিনারদের জন্য, যেখানে কোন কোডিং নলেজ ছাড়াই আপনি জয়েন করতে পারবেন। ',
    img : {
        src: 'images/dualphone.png',
        alt: 'dual phone',
        class: 'img-fluid'
    },
    link: {
        href : "https://ostad.app/course/data-science-with-python",
    }
}

</script>

<template>
    <div class="section">
          <div class="container">
              <div class="row">
                  <div class="col-md-6">
                      <img v-bind="launchPhone.img" />
                  </div>
                  <div class="col-md-6 d-flex align-items-center">
                        <div>
                            <div class="box-icon"><span class="ti-rocket gradient-fill ti-3x"></span></div>
                            <h2>{{ launchPhone.title }}</h2>
                            <p class="mb-4">{{ launchPhone.summary }}</p>
                            <a target="_blank" v-bind="launchPhone.link" class="btn btn-primary">READ MORE</a>
                        </div>
                  </div>
              </div>
          </div>
      </div>
</template>
<style scoped>

</style>
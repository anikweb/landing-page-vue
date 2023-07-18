<script setup>
const faq = {
    title : 'Frequently Asked Questions',
    subtitle : 'FAQ',
    items: [
        {
            question : 'Can I try before I buy?',
            answer : 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer rutrum, urna eu pellentesque pretium, nisi nisi fermentum enim, et sagittis dolor nulla vel sapien. Vestibulum sit amet mattis ante.'
        },
        {
            question : 'What payment methods do you accept?',
            answer : 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer rutrum, urna eu pellentesque pretium, nisi nisi fermentum enim, et sagittis dolor nulla vel sapien. Vestibulum sit amet mattis ante.'
        },
        {
            question : 'Can I change my plan later?',
            answer : 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer rutrum, urna eu pellentesque pretium, nisi nisi fermentum enim, et sagittis dolor nulla vel sapien. Vestibulum sit amet mattis ante.'
        },
        {
            question : 'Do you have a contract?',
            answer : 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer rutrum, urna eu pellentesque pretium, nisi nisi fermentum enim, et sagittis dolor nulla vel sapien. Vestibulum sit amet mattis ante.'
        }
    ]
}
</script>

<template>
     <div class="section pt-0">
          <div class="container">
              <div class="section-title">
                  <small>{{faq.subtitle}}</small>
                  <h3>{{faq.title}}</h3>
              </div>

              <div class="row pt-4">
                <div v-for="(item, index) in faq.items" :key="index" class="col-md-6">
                    <h4 class="mb-3">{{ item.question }}</h4>
                      <p class="light-font mb-5"> {{ item.answer }}</p>
                </div>
              </div>
          </div>
      </div>
</template>


<script setup>
const footer = {
    copyright: '<small>COPYRIGHT © 2023. ALL RIGHTS RESERVED. Designed by <a target="_blank" href="https://portfolio.aniksoft.com">ANIK KUMAR NANDI</a></small>',
    links: [
        { name: 'PRESS', url: '#'},
        { name: 'TERMS', url: '#'},
        { name: 'PRIVACY', url: '#'},
    ]
}
</script>

<template>
    <footer class="my-5 text-center">
              <!-- Copyright removal is not prohibited! -->
              <p class="mb-2"  v-html="footer.copyright"></p>

              <small>
                  <a v-for="(link, index) in footer.links" :key="index" :href="link.url" class="m-2">{{ link.name }}</a>
              </small>
          </footer>
</template>
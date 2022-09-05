<template>
  <div class="body">
    <div class="page">
      <MainHeader />
      <MainContent />
      <Footer />
    </div>
  </div>

</template>

<script>
import MainContent from './MainContent.vue';
import MainHeader from './MainHeader.vue';
import Footer from './Footer.vue';
export default {
  components: {
    MainHeader,
    MainContent,
    Footer
},
  data() {
    return {

    }
  },
  methods: {

  }
}
</script>

<style>
/* @import url('https://fonts.googleapis.com/css2?family=Source+Sans+Pro:wght@400;900&display=swap'); */
/* @import url('https://fonts.googleapis.com/css2?family=Source+Sans+Pro:wght@300;400;900&display=swap'); */
@import url('https://fonts.googleapis.com/css2?family=Source+Sans+Pro:wght@300;400;600;900&display=swap');
/* @import url('https://fonts.googleapis.com/css2?family=Inter&family=Source+Sans+Pro:wght@300;400;600;900&display=swap'); */
/* @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400&family=Source+Sans+Pro:wght@300;400;600;900&display=swap'); */
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@300&family=Source+Sans+Pro:wght@300;400;600;900&display=swap');

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Source Sans Pro', sans-serif;
}

.body {
  padding: 32px;
  background: rgba(255, 254, 251, 0.8);
}

.page {
  max-width: 1440px;
  margin: 0 auto;
}

@media (max-width: 766px) {
  .body {
    padding: 16px;
  }
}
</style>
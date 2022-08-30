<template>
  <div class="body">
    <div class="page">
      <main-header />
      <div class>

      </div>
    </div>
  </div>

</template>

<script>
import MainHeader from './MainHeader.vue'
export default {
  components: {
    MainHeader
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

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Source Sans Pro', sans-serif;
}

.body {
  padding: 32px;
}

.page {
  max-width: 1440px;
  margin: 0 auto;
  border: 1px solid red;
}
</style>
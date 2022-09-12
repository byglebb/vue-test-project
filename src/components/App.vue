<template>
  <div class="body">
    <div class="page">
      <!-- <MainHeader :cardsList="cardsList" /> -->
      <MainHeader />
      <!-- <MainContent @open="openPopup" @cards="checkCards" /> -->
      <MainContent @open="openPopup" />
      <tooltip-popup v-model:open="visibleState" />
      <MainFooter />
    </div>
  </div>

</template>

<script>
import MainContent from './MainContent.vue';
import MainHeader from './MainHeader.vue';
import MainFooter from './MainFooter.vue';

export default {
  components: {
    MainHeader,
    MainContent,
    MainFooter,
  },
  data() {
    return {
      visibleState: false,
      // cardsList: this.checkCards,
    }
  },
  methods: {
    openPopup() {
      this.visibleState = true;
    },
    // checkCards(initialCards) {
    //   const interpList = initialCards.slice();
    //   console.log(initialCards);
    //   console.log(interpList);
    //   this.cardsList.push(interpList);
    //   console.log(this.cardsList);
    //   return {
    //     interpList
    //   }
    // },
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Source+Sans+Pro:wght@300;400;600;900&display=swap');
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
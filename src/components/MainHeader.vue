<template>
  <header class="header">
    <h2 class="header__title">Добавление товара</h2>
    <dropdown-list v-model="selectedSort" :options="sortOptions" />
  </header>
</template>

<script>
export default {
  // props: {
  //   cardsList: {
  //     type: Array,
  //     required: true,
  //   },
  // },
  components: {

  },
  data() {
    return {
      selectedSort: '',
      sortOptions: [
        { value: 'min', name: 'По цене min' },
        { value: 'max', name: 'По цене max' }
      ]
    }
  },
  methods: {

  },
  watch: {
    selectedSort(newValue) {
      console.log(newValue);
      // console.log(this.cardsList);
      // this.cardsList.sort((card1, card2) => {
        
      // })
    },
  }
}
</script>

<style scoped>
.header {
  display: flex;
  justify-content: space-between;
}

.header__title {
  font-style: normal;
  font-weight: 600;
  font-size: 28px;
  line-height: 35px;
  color: #3F3F3F;
}

@media (max-width: 766px) {
  .header__title {
    font-style: normal;
    font-weight: 600;
    font-size: 22px;
    line-height: 35px;
    color: #3F3F3F;
  }
}
</style>
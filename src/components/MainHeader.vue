<template>
  <header class="header">
    <h2 class="header__title">Добавление товара</h2>
    <select class="header__select">
      <option class="header__option">По умолчанию</option>
      <!-- <option class="header__option">По возрастанию цены</option>
      <option class="header__option">По убыванию цены</option> -->
    </select>
  </header>
</template>

<script>
export default {
  components: {

},
  data() {
    return {

    }
  },
  methods: {

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

.header__select {
  background: #FFFEFB;
  box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
  border-radius: 4px;
  /* padding-top: 10px;
  padding-bottom: 10px;
  padding-left: 16px; */
  padding: 10px 16px;
  border: none;
}

.header__option {
  font-style: normal;
  font-weight: 400;
  font-size: 12px;
  line-height: 15px;
}
</style>
<template>
  <select class="header__select" v-model="modelValue" @change="changeOption">
    <option disabled value="">По умолчанию</option>
    <option v-for="option in options" :key="option.value" :value="option.value">{{option.name}}</option>
  </select>
</template>

<script>
export default {
  name: 'dropdown-list',
  props: {
    modelValue: {
      type: String //поле по которому будет идти сортировка
    },
    options: {
      type: Array,
      default: () => []
    }
  },
  methods: {
    changeOption(event) {
      this.$emit('update:modelValue', event.target.value)
    }
  }

}
</script>

<style scoped>
.header__select {
  background: #FFFEFB;
  box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
  border-radius: 4px;
  /* padding-top: 9px;
  padding-bottom: 9px;
  padding-left: 16px; */
  padding: 9px 16px;
  border: none;
  font-family: 'Source Sans Pro';
  font-style: normal;
  font-weight: 400;
  font-size: 12px;
  line-height: 15px;
  color: #B4B4B4;
}
</style>
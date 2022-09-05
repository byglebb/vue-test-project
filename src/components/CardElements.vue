<template>
  <section class="elements">
    <CardItem 
      v-for="card in initialCards" 
      :card="card" 
      :key="card.id"
      @remove="$emit('remove', card)"
    />
  </section>
</template>

<script>
import CardItem from "./CardItem.vue";
export default {
    components: { CardItem },
    props: {
        initialCards: {
            type: Array,
            required: true,
        },
    }
}
</script>

<style scoped>
.elements {
  min-width: 332px;
  display: grid;
  margin-left: auto;
  margin-right: auto;
  max-width: calc(100% - 348px);
  grid-template-columns: repeat(auto-fit, 332px);
  grid-template-rows: repeat(2, 1fr);
  justify-content: center;
  gap: 16px;
}
</style>

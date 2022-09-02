<template>
  <main class="content">
    <AddBar />
    <CardElements />
  </main>
</template>

<script>
import AddBar from "./AddBar.vue";
import CardElements from "./CardElements.vue";
export default {
  components: {
    AddBar,
    CardElements
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
.content {
  max-width: 100%;
  display: flex;
  /* border: 1px solid red; */
  margin-top: 16px;
}

@media (max-width: 766px) {
  .content {
    flex-direction: column;
  }
}
</style>
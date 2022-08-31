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
  display: flex;
  border: 1px solid red;
  margin-top: 16px;
}
</style>
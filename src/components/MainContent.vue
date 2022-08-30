<template>
  <main class="content">
    <section class="addbar">

    </section>
    <section class="elements">
      <article class="element">
      </article>
      <article class="element">
      </article>
      <article class="element">
      </article>
      <article class="element">
      </article>
      <article class="element">
      </article>
      <article class="element">
      </article>
      </section>
  </main>
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
.content {
  display: flex;
  border: 1px solid red;
  margin-top: 16px;
}

.addbar {
  display: flex;
  flex-direction: column;
  padding: 24px;
  width: 332px;
  height: 440px;
  border: 1px solid red;
  margin-right: 16px;

  /* position: sticky; */
}

.elements {
  display: grid;
  /* margin-left: auto; */
  margin-right: 0;
  max-width: calc(100% - 348px);
  grid-template-columns: repeat(auto-fit, 332px);
  grid-template-rows: repeat(2, 1fr);
  justify-content: center;
  gap: 16px;
  border: 1px solid blue;
}

.element {
  display: flex;
  flex-direction: column;
  position: relative;
    border: 1px solid green;
}
</style>
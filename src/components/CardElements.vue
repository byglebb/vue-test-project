<template>
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
</template>

<script>

</script>

<style>
.elements {
  display: grid;
  margin-left: auto;
  margin-right: auto;
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
  height: 423px;
  background: #FFFEFB;
  box-shadow: 0px 20px 30px rgba(0, 0, 0, 0.04), 0px 6px 10px rgba(0, 0, 0, 0.02);
  border-radius: 4px;
}
</style>
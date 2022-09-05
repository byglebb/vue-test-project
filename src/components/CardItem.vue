<template>
  <article class="element">
    <button class="element__delete-button" type="button" @click="$emit('remove', card)"></button>
    <img class="element__image" v-bind:src="card.link" v-bind:alt="card.name" />
    <div class="element__description-container">
      <h2 class="element__name">{{ card.name }}</h2>
      <p class="element__description">{{ card.description }}</p>
      <p class="element__price">{{ card.price }}</p>
    </div>
  </article>
</template>

<script>
export default {
  props: {
    card: {
      type: Object,
      required: true,
    }
  }
}
</script>

<style scoped>
.element {
  /* cursor: pointer; */
  display: flex;
  flex-direction: column;
  position: relative;
  height: 423px;
  background: #fffefb;
  box-shadow: 0px 20px 30px rgba(0, 0, 0, 0.04), 0px 6px 10px rgba(0, 0, 0, 0.02);
  border-radius: 4px;
}

.element__delete-button {
  position: absolute;
  right: -12px;
  top: -10px;
  cursor: pointer;
  border: none;
  background: none;
  width: 40px;
  height: 40px;
  background-image: url(../images/delete_button.svg);
}

.element__delete-button:hover {
  opacity: 0.8;
  transition: 0.5s;
}

.element__image {
  border-radius: 4px 4px 0px 0px;
  width: 332px;
  height: 200px;
}

.element__description-container {
  display: flex;
  flex-direction: column;
  width: 332px;
  height: 223px;
  padding: 16px 16px 24px 16px;
}

.element__name {
  font-family: "Source Sans Pro";
  font-style: normal;
  font-weight: 600;
  font-size: 20px;
  line-height: 25px;
  color: #3f3f3f;
  text-overflow: ellipsis;
  white-space: nowrap;
  overflow: hidden;
}

.element__description {
  font-family: "Source Sans Pro";
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  line-height: 20px;
  color: #3f3f3f;
  margin-top: 16px;
  height: 80px;
  /* text-overflow: ellipsis;
  white-space: nowrap; */
  overflow: hidden;
}

.element__price {
  font-family: "Source Sans Pro";
  font-style: normal;
  font-weight: 600;
  font-size: 24px;
  line-height: 30px;
  color: #3f3f3f;
  margin-top: 32px;
}
</style>
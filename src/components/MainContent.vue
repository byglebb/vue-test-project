<template>
  <main class="content">
    <AddBar @add="createCard" @open="$emit('open')"/>
    <CardElements 
      v-bind:initialCards="initialCards" 
      @remove="removeCard"
      />
  </main>
</template>

<script>
import AddBar from "./AddBar.vue";
import CardElements from "./CardElements.vue";
export default {
  components: {
    AddBar,
    CardElements,
  },
  data() {
    return {
      initialCards: [
        {
          id: 1,
          name: "Архыз",
          description:
            "Это кавказский хребет Это кавказский хребет Это кавказский хребетЭто кавказский хребет Это кавказский хребет",
          link:
            "https://pictures.s3.yandex.net/frontend-developer/cards-compressed/arkhyz.jpg",
          price: "12 300 руб.",
        },
        {
          id: 2,
          name: "Челябинская область",
          description: "А это ЧЕЛЯБИНСК А это ЧЕЛЯБИНСК А это ЧЕЛЯБИНСК",
          link:
            "https://pictures.s3.yandex.net/frontend-developer/cards-compressed/chelyabinsk-oblast.jpg",
          price: "33 433 400 руб.",
        },
        {
          id: 3,
          name: "Иваново",
          description:
            "Город невест Город невест Город невестГород невест Город невест Город невест Город невест",
          link:
            "https://pictures.s3.yandex.net/frontend-developer/cards-compressed/ivanovo.jpg",
          price: "300 руб.",
        },
        {
          id: 4,
          name: "Камчатка",
          description:
            "Вулканы, красота: Дорого! Вулканы, красота: Дорого! Вулканы, красота: Дорого!Вулканы, красота: Дорого! Вулканы, красота: Дорого! Вулканы, красота: Дорого!",
          link:
            "https://pictures.s3.yandex.net/frontend-developer/cards-compressed/kamchatka.jpg",
          price: "1 000 000 руб.",
        },
        {
          id: 5,
          name: "Холмогорский район",
          description: "Ноу нейм для меня",
          link:
            "https://pictures.s3.yandex.net/frontend-developer/cards-compressed/kholmogorsky-rayon.jpg",
          price: "5000 руб.",
        },
        {
          id: 6,
          name: "Байкал",
          description:
            "Самое полноводное озеро в мире. Самое полноводное озеро в мире. Самое полноводное озеро в мире.",
          link:
            "https://pictures.s3.yandex.net/frontend-developer/cards-compressed/baikal.jpg",
          price: "Беcценно!",
        },
      ],
    };
  },
  methods: {
    createCard(newCard) {
      console.log(newCard);
      this.initialCards.unshift(newCard);
    },
    removeCard(card) {
      this.initialCards = this.initialCards.filter((c) => c.id !== card.id)
    },
  },
};
</script>

<style scoped>
.content {
  max-width: 100%;
  display: flex;
  margin-top: 16px;
}

@media (max-width: 766px) {
  .content {
    flex-direction: column;
  }
}
</style>

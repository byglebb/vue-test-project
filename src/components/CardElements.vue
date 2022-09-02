<template>
  <section class="elements">
    <article class="element" v-for="card in initialCards">
      <button class="element__delete-button" type="button"></button>
      <img class="element__image" v-bind:src="card.link" v-bind:alt="card.name">
      <div class="element__description-container">
        <h2 class="element__name">{{card.name}}</h2>
        <p class="element__description">{{card.description}}</p>
        <p class="element__price">{{card.price}}</p>
      </div>
    </article>

    <!-- <article class="element">
      <button class="element__delete-button" type="button"></button>
      <img class="element__image" src="../images/Picture.png">
      <div class="element__description-container">
        <h2 class="element__name">Наименование товара Наименование товара</h2>
        <p class="element__description">Довольно-таки интересное описание товара в несколько строк. Довольно-таки
          интересное описание товара в несколько строк ки интересное описание товара в несколько строк. Довольно-таки
          интересное</p>
        <p class="element__price">10 000 руб.</p>
      </div>
    </article>

    <article class="element">
      <button class="element__delete-button" type="button"></button>
      <img class="element__image" src="../images/Picture.png">
      <div class="element__description-container">
        <h2 class="element__name">Наименование товара Наименование товара</h2>
        <p class="element__description">Довольно-таки интересное описание товара в несколько строк. Довольно-таки
          интересное описание товара в несколько строк ки интересное описание товара в несколько строк. Довольно-таки
          интересное</p>
        <p class="element__price">10 000 руб.</p>
      </div>
    </article> -->
  </section>
</template>

<script>
import { initialCards } from './constants.js';
export default {
  data() {
    return {
      initialCards: [
        {
          name: 'Архыз',
          description: 'Это кавказский хребет Это кавказский хребет Это кавказский хребетЭто кавказский хребет Это кавказский хребет',
          link: 'https://pictures.s3.yandex.net/frontend-developer/cards-compressed/arkhyz.jpg',
          price: '12 300 руб.'
        },
        {
          name: 'Челябинская область',
          description: 'А это ЧЕЛЯБИНСК А это ЧЕЛЯБИНСК А это ЧЕЛЯБИНСК',
          link: 'https://pictures.s3.yandex.net/frontend-developer/cards-compressed/chelyabinsk-oblast.jpg',
          price: '300 руб.'
        },
        {
          name: 'Иваново',
          description: 'Город невест Город невест Город невестГород невест Город невест Город невест Город невест',
          link: 'https://pictures.s3.yandex.net/frontend-developer/cards-compressed/ivanovo.jpg',
          price: '300 руб.'
        },
        {
          name: 'Камчатка',
          description: 'Вулканы, красота: Дорого! Вулканы, красота: Дорого! Вулканы, красота: Дорого!Вулканы, красота: Дорого! Вулканы, красота: Дорого! Вулканы, красота: Дорого!',
          link: 'https://pictures.s3.yandex.net/frontend-developer/cards-compressed/kamchatka.jpg',
          price: '1 000 000 руб.'
        },
        {
          name: 'Холмогорский район',
          description: 'Ноу нейм для меня',
          link: 'https://pictures.s3.yandex.net/frontend-developer/cards-compressed/kholmogorsky-rayon.jpg',
          price: '5 000 руб.'
        },
        {
          name: 'Байкал',
          description: 'Самое полноводное озеро в мире. Самое полноводное озеро в мире. Самое полноводное озеро в мире.',
          link: 'https://pictures.s3.yandex.net/frontend-developer/cards-compressed/baikal.jpg',
          price: 'Беcценно!'
        }
      ]
    }
  },
  methods: {
    createCard() {
      console.log(initialCards.name);
    }
  }
}

</script>

<style>
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
  /* border: 1px solid blue; */
}

.element {
  /* cursor: pointer; */
  display: flex;
  flex-direction: column;
  position: relative;
  height: 423px;
  background: #FFFEFB;
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
  opacity: .8;
  transition: .5s;
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
  font-family: 'Source Sans Pro';
  font-style: normal;
  font-weight: 600;
  font-size: 20px;
  line-height: 25px;
  color: #3F3F3F;
  text-overflow: ellipsis;
  white-space: nowrap;
  overflow: hidden;
}

.element__description {
  font-family: 'Source Sans Pro';
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  line-height: 20px;
  color: #3F3F3F;
  margin-top: 16px;
  height: 80px;
  /* text-overflow: ellipsis;
  white-space: nowrap; */
  overflow: hidden;
}

.element__price {
  font-family: 'Source Sans Pro';
  font-style: normal;
  font-weight: 600;
  font-size: 24px;
  line-height: 30px;
  color: #3F3F3F;
  margin-top: 32px;
}
</style>
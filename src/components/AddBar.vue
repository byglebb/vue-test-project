<template>
  <section class="addbar">
    <form class="addbar__form">
      <label for="name" class="addbar__form-label">Наименование товара
        <div class="addbar__dot"></div>
      </label>
      <input type="text" id="name" class="addbar__form-item" placeholder="Введите наименование товара" required>
      <span class="addbar__input-error"></span>

      <label for="description" class="addbar__form-label">Описание товара
      </label>
      <textarea type="text" id="description" class="addbar__form-item addbar__form-item_description"
        placeholder="Введите описание товара"></textarea>

      <label for="url" class="addbar__form-label">Ссылка на изображение товара
        <div class="addbar__dot"></div>
      </label>
      <input type="url" id="url" class="addbar__form-item" placeholder="Введите ссылку" required>
      <span class="addbar__input-error"></span>

      <label for="price" class="addbar__form-label">Цена товара
        <div class="addbar__dot"></div>
      </label>
      <input type="text" id="price" class="addbar__form-item" placeholder="Введите цену" required>
      <span class="addbar__input-error"></span>

      <button class="addbar__button" type="button">Добавить товар</button>
    </form>
  </section>
</template>

<script>

</script>

<style scoped>
.addbar {
  /* display: flex;
  flex-direction: column; */
  padding: 24px;
  width: 332px;
  height: 440px;
  /* border: 1px solid red; */
  margin-right: 16px;
  background: #FFFEFB;
  box-shadow: 0px 20px 30px rgba(0, 0, 0, 0.04), 0px 6px 10px rgba(0, 0, 0, 0.02);
  border-radius: 4px;

  position: sticky;
  top: 24px;
}

.addbar__form {
  display: flex;
  flex-direction: column;
  /* border: 1px solid peru; */
}

.addbar__form-label {
  display: flex;
  font-style: normal;
  font-weight: 400;
  font-size: 10px;
  line-height: 13px;
  letter-spacing: -0.02em;
  color: #49485E;
  margin-bottom: 4px;
}

.addbar__dot {
  width: 4px;
  height: 4px;
  background: #FF8484;
  border-radius: 50%;
}

.addbar__form-item {
  font-style: normal;
  font-weight: 400;
  font-size: 12px;
  line-height: 15px;
  padding: 10px 16px;
  background: #FFFEFB;
  box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
  border-radius: 4px;
  border: none;
  height: 36px;
  margin-bottom: 4px;
}

.addbar__form-item_description {
  height: 108px;
  resize: none;
  margin-bottom: 16px;
}

.addbar__form-item_type_error {
  border: 1px solid #FF8484;
}

.addbar__input-error {
  min-height: 10px;
  font-family: 'Source Sans Pro';
  font-style: normal;
  font-weight: 400;
  font-size: 8px;
  line-height: 10px;
  letter-spacing: -0.02em;
  color: #FF8484;
  margin-bottom: 2px;
}

.addbar__input-error_active {
  display: block;
}

.addbar__button {
  border: none;
  margin-top: 8px;
  font-family: 'Inter';
  background: #7BAE73;
  color: #fff;
  border-radius: 10px;
  height: 36px;
  font-style: normal;
  font-weight: 600;
  font-size: 12px;
  line-height: 15px;
  text-align: center;
  box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.1);
  cursor: pointer;

}

.addbar__button:hover {
  opacity: .8;
  transition: .5s;
}

.addbar__button_disabled {
  color: #B4B4B4;
  background: #EEEEEE;
  letter-spacing: -0.02em;
  opacity: 1;
}

.addbar__button_disabled:hover {
  opacity: 1;
}
</style>
<template>
  <div class="popup" v-if="open" @click="closePopup">
    <div class="popup__window" @click.stop>
      <button class="popup__close-button" type="button" @click="closePopup"></button>
      <img class='popup__picture' src='../../images/Pic_success.svg' alt='Подтверждение добавления' />
      <h2 class="popup__text">Товар успешно добавлен!</h2>
    </div>
  </div>
</template>

<script>
export default {
  name: 'tooltip-popup',
  props: {
    open: {
      type: Boolean,
      default: false
    }
  },
  methods: {
    closePopup() {
      this.$emit('update:open', false);
    }
  }
}
</script>

<style scoped>
.popup {
  display: flex;
  position: fixed;
  z-index: 100;
  color: #000;
  background: rgba(0, 0, 0, 0.5);
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  /* opacity: 0; */
  /* visibility: hidden; */
  /* transition: visibility .3s, opacity .3s linear; */
}

.popup__window {
  margin: auto;
  background: white;
  border-radius: 4px;
  width: 430px;
  height: 300px;
  padding: 24px;
  display: flex;
  flex-direction: column;
  position: relative;
}

.popup__close-button {
  position: absolute;
  padding: 0 0;
  margin: 0 0;
  right: -40px;
  top: -40px;
  cursor: pointer;
  border: none;
  background: none;
  height: 32px;
  width: 32px;
  background-image: url(../../images/Close_button.svg);
}

.popup__close-button:hover {
  opacity: .5;
  transition: .5s;
}

.popup__picture {
  width: 120px;
  height: 120px;
  align-self: center;
  margin-top: 35px;
  margin-bottom: 32px;
}

.popup__text {
  font-style: normal;
  font-weight: 900;
  font-size: 24px;
  line-height: 29px;
  color: #000;
  margin-left: 36px;
  margin-right: 36px;
  margin-bottom: 60px;
  text-align: center;
}

@media (max-width: 766px) {
  .popup__window {
    width: 320px;
    height: 230px;
  }

  .popup__close-button {
    right: 0px;
    top: -36px;
    height: 20px;
    width: 20px;
    background-size: 20px;
  }

  .popup__text {
    font-size: 18px;
    line-height: 22px;
    margin-left: 22px;
    margin-right: 22px;
  }

  .popup__picture {
  width: 90px;
  height: 90px;
  align-self: center;
  margin-top: 15px;
  margin-bottom: 32px;
  }
}
</style>
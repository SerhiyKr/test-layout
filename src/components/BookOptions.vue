<template>
  <div class="book__options">
    <span class="labels label__rooms">{{ textRooms }}</span>
    <input class="input__room input__room-number" type="number" :value="value1"/>
    <img :src="buttonUp" alt="Добавить номер" class="buttons_up-down button__up-room-number"
         v-on:click="value1 >= maxValue ? value1 = 1 : value1++;">
    <img :src="buttonDown" alt="Убрать номер" class="buttons_up-down button__down-room-number"
         v-on:click="value1 >= minValue ? value1 = 1 : value1--">
    <span class="labels label__adults">{{ textAdult }}</span>
    <input class="input__room input__room-number2" type="number" :value="value2"/>
    <img :src="buttonUp" alt="Добавить номер" class="buttons_up-down button__up-room-number2"
         v-on:click="value2 >= maxValue ? value2 = 1 : value2++;">
    <img :src="buttonDown" alt="Убрать номер" class="buttons_up-down button__down-room-number2"
         v-on:click="value2 >= minValue ? value2 = 1 : value2--">
    <span class="labels label__childrens">{{ textChildren }}</span>
    <input class="input__room input__room-number3" type="number" :value="value3"/>
    <img :src="buttonUp" alt="Добавить номер" class="buttons_up-down button__up-room-number3"
         v-on:click="value3 >= maxValue ? value3 = 1 : value3++;">
    <img :src="buttonDown" alt="Убрать номер" class="buttons_up-down button__down-room-number3"
         v-on:click="value3 >= minValue ? value3 = 0 : value3--">
    <img :src="circle" class="image__plus-circle" alt="Плюс">
  </div>
</template>

<script>
import buttonUp from '@/assets/images/buttonUp.png';
import buttonDown from '@/assets/images/buttonDown.png';
import circle from '@/assets/images/circle.png';

export default {
  name: "BookOptions",
  data() {
    return {
      maxValue: 10,
      minValue: 0,
      value1: 1,
      value2: 1,
      value3: 0,
      textRooms: "Номера",
      textAdult: "Взрослые",
      textChildren: "Дети",
      buttonUp,
      buttonDown,
      circle
    }
  }
}
</script>

<style scoped>
.book__options {
  width: 27%;
  height: 100px;
  display: flex;
  transform: matrix(1, 0, 0, 1, -49, 0);
}
.input__room {
  height: 27px;
  width: 27px;
  border-radius: 0;
  border: 2px #8b9198 solid;
  color: #8b9198;
  font-family: Avenir NextCyr;
  font-weight: 500;
  font-size: 16pt;
  text-align: center;
}
.input__room-number {
  transform: matrix(1, 0, 0, 1, 65, 43);
}
input[type=number]::-webkit-inner-spin-button,
input[type=number]::-webkit-outer-spin-button {
  -webkit-appearance: none;
  margin: 0;
}
.buttons_up-down {
  height: 10px;
  width: 13px;
}
.button__up-room-number {
  transform: matrix(1, 0, 0, 1, 73, 44);
}
.button__down-room-number {
  transform: matrix(1, 0, 0, 1, 60, 65);
}
.input__room-number2 {
  transform: matrix(1, 0, 0, 1, 126, 43);
}
.button__up-room-number2 {
  transform: matrix(1, 0, 0, 1, 134, 44);
}
.button__down-room-number2 {
  transform: matrix(1, 0, 0, 1, 121, 65);
}
.input__room-number3 {
  transform: matrix(1, 0, 0, 1, 193, 43);
}
.button__up-room-number3 {
  transform: matrix(1, 0, 0, 1, 200, 44);
}
.button__down-room-number3 {
  transform: matrix(1, 0, 0, 1, 187, 65);
}
.labels {
  position: fixed;
  font-size: 12pt;
  font-family: Myriad Pro;
  font-weight: 400;
}
.label__rooms {
  transform: matrix(1, 0, 0, 1, 63, 23);
}
.label__adults {
  transform: matrix(1, 0, 0, 1, 185, 23);
}
.label__childrens {
  transform: matrix(1, 0, 0, 1, 314, 23);
}
.image__plus-circle {
  width: 43px;
  height: 43px;
  transform: matrix(1, 0, 0, 1, 219, 31);
}
</style>
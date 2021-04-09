<template>
  <div class="search__input">
    <label for="hotel-search__input" class="input__text">{{ inputText }}</label>
    <img class="image__location" :src="imageLocation" alt="Локация">
    <input id="hotel-search__input" class="city__input" type="text" placeholder="Введите здесь место">
  </div>
</template>

<script>
import imageLocation from "@/assets/images/location.png"

export default {
  name: "SerchInput",
  data () {
    return {
      inputText: "Место или название отеля",
      imageLocation
    }
  }
}
</script>

<style scoped>
.search__input {
  width: 23%;
  height: 100px;
}
.input__text {
  font-family: Myriad Pro;
  font-weight: 400;
  font-size: 12pt;
  position: fixed;
  transform: matrix(1, 0, 0, 1, 73, 24);
}
.city__input {
  font-family: Fira Sans;
  font-size: 18pt;
  font-weight: bold;
  font-style: italic;
  border: none;
  position: fixed;
  transform: matrix(1, 0, 0, 1, 103, 46);
  outline: none;
}
.image__location {
  position: fixed;
  transform: matrix(1, 0, 0, 1, 72, 49);
  width: 20px;
  height: 25px;
}
</style>
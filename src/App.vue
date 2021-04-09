<template>
  <div id="app">
    <app-main></app-main>
  </div>
</template>

<script>
import MainComponent from "@/components/MainComponent";

export default {
  name: 'App',
  components: {
    appMain: MainComponent
  }
}
</script>

<style>
.mx-input {
  border: none;
  -webkit-box-shadow: none;
  font-family: Fira Sans;
  font-weight: bold;
  font-size: 18pt;
  color: black;
}
.mx-icon-calendar {
  z-index: -10;
}
#date-picker__input {
  height: 35%;
  transform: matrix(1, 0, 0, 1, 62, 44);
}
#date-picker__input2 {
  height: 35%;
  transform: matrix(1, 0, 0, 1, 100, 44);
}
#date-picker__input > div > i {
  z-index: -1;
}
@media screen and (max-width: 1777px) {
  #app .search__wrapper {
    height: 200px;
    display: flex;
    flex-direction: column;
  }
  #app .button__search-button {
    margin: auto;
    transform: matrix(1, 0, 0, 1, 0, 0);
  }
  #app #app2 {
    justify-content: space-evenly;
  }
}
@media screen and (max-width: 1460px) {
  #app .search__wrapper {
    height: 400px;
    display: flex;
    flex-direction: column;
  }
  #app #app2 {
    display: flex;
    flex-direction: column;
    height: 300px;
  }
  #app #app2 .search__input, .date__input, .book__options {
    padding: 0;
    margin: auto;
  }
  #app #app2 .search__input {
    width: 39%;
  }
  #app #app2 .date__input {
    width: 55%;
  }
  #app #app2 .book__options {
    width: 35%;
  }
}
@media screen and (max-width: 882px) {
  #app #app2 .search__input {
    width: 45%;
  }
  #app #app2 .date__input {
    width: 66%;
  }
  #app #app2 .book__options {
    width: 43%;
  }
}
@media screen and (max-width: 726px) {
  #app #app2 .search__input, .date__input, .book__options {
    padding: 0;
    margin: inherit;
  }
  #app .input__text {
    transform: matrix(1, 0, 0, 1, 0, 24);
  }
  #app .image__location {
    transform: matrix(1, 0, 0, 1, 0, 49);
  }
  #app .city__input {
    transform: matrix(1, 0, 0, 1, 34, 46);
  }
  #app .date__input {
    display: flex;
    flex-direction: column;
    height: 232px;
  }
  #app .image-mark1 {
    display: none;
  }
  #app .image-mark2 {
    transform: matrix(1, 0, 0, 1, 97, 35);
  }
  #app .date-picker__input2 {
    transform: matrix(1, 0, 0, 1, 62, 44)
  }
  #app .label__start-text,
  #app .label__finish-text {
    display: none;
  }
  #app .image-calendar {
    transform: matrix(1, 0, 0, 1, 37, 79);
  }
  #app .button__search-button {
    margin: initial;
    transform: matrix(1, 0, 0, 1, 0, 39)
  }
}
</style>

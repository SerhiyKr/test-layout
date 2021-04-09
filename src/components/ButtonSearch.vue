<template>
    <button class="button__search-button">{{ textButton }}</button>
</template>

<script>
export default {
  name: "ButtonSearch",
  data () {
    return {
      textButton: "Найти"
    }
  }
}
</script>

<style scoped>
.button__search-button {
  transform: matrix(1, 0, 0, 1, -12, 15);
  width: 265px;
  height: 70px;
  background: #ed9915;
  border: none;
  border-radius: 4px;
  font-family: Proxima Nova;
  font-weight: bold;
  color: white;
  font-size: 25px;
  text-transform: uppercase;
}
</style>
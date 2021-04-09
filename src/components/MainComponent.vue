<template>
  <div class="search__wrapper">
    <div id="app2">
      <app-search></app-search>
      <app-date></app-date>
      <app-book></app-book>
    </div>
    <app-button></app-button>
  </div>
</template>

<script>
import SearchInput from "@/components/SearchInput";
import DateInput from "@/components/DateInput";
import BookOptions from "@/components/BookOptions";
import ButtonSearch from "@/components/ButtonSearch";

export default {
  name: "MainComponent",
  components: {
    appSearch: SearchInput,
    appDate: DateInput,
    appBook: BookOptions,
    appButton: ButtonSearch
  }
}
</script>

<style scoped>
#app2 {
  width: 100%;
  height: 100px;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
.search__wrapper {
  height: 100px;
  width: 100%;
  margin: auto;
  display: flex;
}
</style>
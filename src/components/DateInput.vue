<template>
    <div class="date__input">
<!--      <img :src="line" alt="imageLine" class="line image-line1">-->
      <label class="label__start-text">{{ textStart }}</label>
      <label class="label__finish-text">{{ textFinish }}</label>
        <date-picker id="date-picker__input" class="date-picker__input" v-model="value1" locale="ru-ru" format="D MMMM" placeholder="Заезд"></date-picker>
        <img :src="imageCalendar" alt="imageCalendar" class="image-calendar">
        <img :src="imageMark1" alt="imageMark1" class="image-mark1">
        <img :src="imageMark2" alt="imageMark2" class="image-mark2">
        <date-picker id="date-picker__input2" class="date-picker__input2" v-model="value2" lang="ru" format="D MMMM" placeholder="Выезд"></date-picker>
<!--        <img :src="line" alt="imageLine" class="line image-line2">-->
    </div>
</template>

<script>
import DatePicker from 'vue2-datepicker';
import 'vue2-datepicker/index.css';
import imageCalendar from '@/assets/images/calendar.png';
import imageMark1 from '@/assets/images/mark1.png';
import imageMark2 from '@/assets/images/mark2.png';
import line from '@/assets/images/line.png';

export default {
  name: "DateInput",
  components: {
    DatePicker
  },
  data() {
    return {
      textStart: "Заезд",
      textFinish: "Выезд",
      value1: [],
      value2: [],
      imageCalendar,
      imageMark1,
      imageMark2,
      line
    }
  }
}
</script>

<style scoped>
.date__input {
  width: 39%;
  height: 100px;
  display: flex;
}
.label__start-text {
  font-family: Proxima Nova;
  font-size: 12pt;
  font-weight: 400;
  position: fixed;
  transform: matrix(1, 0, 0, 1, 42, 24);
}
.label__finish-text {
  font-family: "Proxima Nova";
  font-size: 12pt;
  font-weight: 400;
  position: fixed;
  transform: matrix(1, 0, 0, 1, 340, 24);
}
.image-calendar {
  position: fixed;
  transform: matrix(1, 0, 0, 1, 37, 47);
  width: 25px;
  height: 25px;
}
.image-mark1 {
  width: 20px;
  height: 10px;
  transform: matrix(1, 0, 0, 1, 362, 55);
}
.image-mark2 {
  height: 6px;
  width: 6px;
  transform: matrix(1, 0, 0, 1, 13, 58);
}
.line {
  width: 3px;
  height: 39px;
}
.image-line1 {
  transform: matrix(1, 0, 0, 1, -25, 33);
}
.image-line2 {
  transform: matrix(1, 0, 0, 1, 48, 33);
}

</style>
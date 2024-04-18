<template>
    <div class="black-bg" v-if="모달창 == true">
    <div class="white-bg">
      <img :src="원룸들[누른거].image">
      <h4>{{ 원룸들[누른거].title }}</h4>
      <p>{{ 원룸들[누른거].content }}</p>
      <input v-model.number="month">
      <!--<input @input="month = $event.target.value">
      <textarea v-model="month"></textarea>
      <select v-model="month">
        <option></option>
        <option></option>
      </select>-->
      <p> {{ month }} 개월 선택함 : {{ 원룸들[누른거].price * month }} 원</p>
      <button @click="closeModal">닫기</button>
    </div>
  </div>
</template>

<script>
export default {
    name : 'Modal',
    data() {
      return {
        month : 1,
      }
    },
    props : {
        원룸들 : Array,
        누른거 : Number,
        모달창 : Boolean,
    },
    methods : {
      closeModal() {
        this.$emit('closeModal')
      }
    }
}
</script>

<style>

</style>
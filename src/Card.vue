<template>
    <div>
    <img :src="원룸들.image" class="room-img">
    <h4 @click="send">{{ 원룸들.title }}</h4>
    <p>{{ 원룸들.price }}원</p>
  </div>
</template>

<script>
export default {
    name : "Card",
    props : {
        원룸들 : Object,
    },
    methods : {
        send(){
            this.$emit('openModal', this.원룸들.id)
        }
    }
}
</script>

<style>

</style>
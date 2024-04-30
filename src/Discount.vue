<template>
    <div class="discount">
        <h4>지금 결제하면 {{ 할인 }}% 할인</h4>
    </div>
</template>

<script>
export default {
    name:'Discount',
    data(){
        return{
            할인 : 30,
        }
    },
    mounted(){
        setInterval(()=>{
            if(this.할인 > 0){
                this.할인 = this.할인 -1;
            }
        }, 1000)
    }
}
</script>

<style>

</style>
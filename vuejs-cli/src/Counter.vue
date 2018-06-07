<template>
    <div class="counter">
        {{ count }}
        <div class="counter__button" v-on:click="increment">
            +
        </div>
    </div>
</template>

<script>
export default {
    data(){
        return{
            count: 0
        }
    },
    methods:{
        increment (){
            this.count++
        }
    }
}
</script>

<style lang="scss">
    .counter{
        font-weight: bold;
        .counter__button{

            border: 5px solid black;
        }
    }
</style>

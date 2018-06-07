<template>
<div>
    <button v-on:click="toggle" class="btn btn-primary">Toggle</button>
    <!-- Permet d'appliquer des classes css -->
    <transition name="bounce" appear>
        <div v-if="visible">
            Lorem ipsum, dolor sit amet consectetur adipisicing elit. Officiis saepe corrupti, magni non tempore sapiente. Mollitia odio inventore praesentium corporis amet iusto architecto consequuntur a eos odit sapiente, ab esse.
        </div>
    </transition>
</div>
</template>

<script>
export default {
    data(){
        return{
            visible: true
        }
    },
    methods: {
        toggle: function (){
            // true = le contraire doncc false / false = le contraire donc true
            this.visible = !this.visible
        }
    }
}
</script>

<style>
/* modifier la classe bounce dans la transition par fade */
    .fade-enter-active, .fade-leave-active{
        transition: opacity 1s, transform 1s;
    }
    .fade-enter, .fade-leave-active{
        opacity: 0;
        transform: translateX(50px);
    }
    
    .bounce-enter-active {
        animation: bounce-in .5s;
    }
    .bounce-leave-active {
    animation: bounce-in .5s reverse;
    }
    @keyframes bounce-in {
        0% {
            transform: scale(0);
        }
        50% {
            transform: scale(1.5);
        }
        100% {
            transform: scale(1);
        }
    }
</style>

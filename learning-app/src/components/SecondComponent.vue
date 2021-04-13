<template>
    <div>
        <ComponentUnderSecond v-if="counter < 0"></ComponentUnderSecond>
        <ComponentUnderSecondPlus v-else></ComponentUnderSecondPlus>
        <h1 v-if="counter === 3">{{title}}</h1>
        <h2 v-else>{{counterWithNum}}</h2>

        <button v-on:click="IncrementCounter()">+1</button>
        <button v-on:click="DecrementCounter()">-1</button><br>
        <button v-on:click="IncrementBy5()">+5</button>
        <button v-on:click="DecrementBy5()">-5</button>
    </div>
</template>


<script>
import ComponentUnderSecond from './ComponentUnderSecond.vue';
import ComponentUnderSecondPlus from './ComponentUnderSecondPlus.vue';
export default {
  components: { ComponentUnderSecond, ComponentUnderSecondPlus },
    data(){
        return{
            title: 'Three',
            counter: 0
        }
    },

    methods:{
        IncrementCounter(){
            this.counter = this.counter + 1;
        },

        DecrementCounter(){
            this.counter = this.counter - 1;
        },

        IncrementBy5(){
            this.counter = this.counter + 5;
        },

        DecrementBy5(){
            this.counter = this.counter - 5;
        }
    },

    watch:{
        counter(){
            
        }
    },

    computed:{
        counterWithNum(){
            return this.counter + ' num'
        }
    }
}
</script>
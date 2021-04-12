<template>
    <div>
        <h1>{{title}}</h1>
        <h2>{{counter}}</h2>

        <button v-on:click="IncrementCounter()">Dodaj 1 do countera</button>
        <button v-on:click="DecrementCounter()">Odejmij 1 od countera</button>
    </div>
</template>


<script>
export default {
    data(){
        return{
            title: 'Second title',
            counter: 0
        }
    },

    methods:{
        IncrementCounter(){
            this.counter = this.counter + 1;
        },

        DecrementCounter(){
            this.counter = this.counter - 1;
        }
    }
}
</script>
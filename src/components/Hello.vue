<template>
    <div class="columns">
        <div class="column text-center">
            <h3>Clicked: {{ $store.state.count }} times, count is {{ evenOrOdd }}.</h3>
            <button class="button is-success" @click="increment">+</button>
            <button class="button is-danger" @click="decrement">-</button>
            <button class="button is-dark" @click="incrementIfOdd">Increment if odd</button>
            <button class="button is-dark" @click="incrementAsync">Increment async</button>
        </div>
    </div>
</template>

<script>

    import {mapGetters, mapActions} from 'vuex'
    export default {
        name: 'hello',
        computed: mapGetters({
            evenOrOdd: 'evenOrOdd'
        }),
        methods: mapActions({
            increment: 'increment',
            decrement: 'decrement',
            incrementIfOdd: 'incrementIfOdd',
            incrementAsync: 'incrementAsync'
        }),
        data () {
            return {
                msg: 'Welcome to Your Vue.js App'
            }
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    h1, h2 {
        font-weight: normal;
    }

    ul {
        list-style-type: none;
        padding: 0;
    }

    li {
        display: inline-block;
        margin: 0 10px;
    }

    a {
        color: #42b983;
    }
</style>

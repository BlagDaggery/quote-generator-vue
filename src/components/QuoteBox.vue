<template>
    <div id="quote-box">
        <div id="text">{{ text }}</div>
        <div id="author">{{ author }}</div>
        <button v-on:click="getQuote">Get a New Quote</button>
    </div>
</template>

<script>
    export default {
        name: 'QuoteBox',
        data: function () {
            return {
                text: '',
                author: ''
            }
        },
        methods: {
            getQuote: function () {
                return fetch('https://simple-quotes-api.herokuapp.com/random')
                    .then(response => response.json())
                    .then(jsonResponse => {
                        this.text = jsonResponse.text;
                        this.author = jsonResponse.author;
                    })
                    .catch(error => console.log(error));
            }
        },
        created: function () {
            this.getQuote();
        }
    }
</script>

<style>
    #quote-box {
        margin: 0 auto;
        border: 1px solid #000;
        max-width: 768px;
        padding: 1rem;
    }
</style>
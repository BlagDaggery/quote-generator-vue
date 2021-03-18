<template>
    <div id="app">
        <HelloWorld msg="Get a Random Quote" />
        <QuoteBox />
    </div>
</template>

<script>
    import HelloWorld from './components/HelloWorld.vue';
    import QuoteBox from './components/QuoteBox.vue';
    
    export default {
      name: 'App',
      components: {
          HelloWorld,
          QuoteBox
      }
    }
</script>

<style>
    #app {
      font-family: Avenir, Helvetica, Arial, sans-serif;
      -webkit-font-smoothing: antialiased;
      -moz-osx-font-smoothing: grayscale;
      text-align: center;
      color: #2c3e50;
      margin-top: 60px;
    }
</style>

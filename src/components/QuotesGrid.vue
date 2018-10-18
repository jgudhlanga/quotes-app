<template>
    <div class="row">
        <app-quote v-for="quote in quotes">{{ quote }}</app-quote>
    </div>
</template>

<script>
    import Quote from './Quote';
    export default {
        name: "QuotesGrid",
        props:['quotes'],
       components: {
          'app-quote': Quote
       }
    }
</script>

<style>

</style>

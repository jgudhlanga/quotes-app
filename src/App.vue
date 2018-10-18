<template>
  <div class="container">
    <app-new-quote @quoteAdded="newQuote"></app-new-quote>
    <app-quote-grid :quotes="quotes"></app-quote-grid>
    <div class="row">
      <div class="col mt-3">
        <div class="alert alert-info text-center" role="alert">
          To Delete a Quote click on it!
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import QuoteGrid from './components/QuotesGrid';
  import NewQuote from './components/NewQuote';
export default {
  name: 'app',
  data () {
    return {
      quotes: [
          'Don’t cry because it’s over, smile because it happened. – (Dr. Seuss)'
      ],
      maxQuotes: 10,
    }
  },
  methods: {
    newQuote(quote) {
       this.quotes.push(quote);
    }
  },
  components: {
    'app-quote-grid': QuoteGrid,
    'app-new-quote': NewQuote
  }
}
</script>

<style lang="scss">

</style>

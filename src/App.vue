<template>
  <div class="container">
    <app-header :quotes-count="quotes.length" :max-quotes="maxQuotes"></app-header>
    <app-new-quote @quoteAdded="newQuote"></app-new-quote>
    <app-quote-grid :quotes="quotes" @quoteDeleted="quoteDeleted"></app-quote-grid>
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
  import Header from './components/Header';
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
      if (this.quotes.length === this.maxQuotes) {
        alert('The maximum quotes reached. Delete some to add new ones');
        return;
      }
       this.quotes.push(quote);
    },
    quoteDeleted(index) {
       this.quotes.splice(index,  1);
    }
  },
  components: {
    'app-quote-grid': QuoteGrid,
    'app-new-quote': NewQuote,
    'app-header': Header,
  }
}
</script>

<style lang="scss">

</style>

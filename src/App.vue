<template>
  <div class="container">
    <new-quote @quoteAdded="newQuote"></new-quote>
    <quote-grid @quoteDeleted="deleteQuote" :quotes="quotes"></quote-grid>
    <div class="row">
      <div class="col-sm-12 text-center">
        <div class="alert alert-info">Info: Click on a Quote to delete it!</div>
      </div>
    </div>
  </div>
</template>

<script>
  import NewQuote from './components/Quotes/NewQuote.vue';
  import QuoteGrid from './components/Quotes/QuoteGrid.vue';

  export default {
    data: () => {
      return {
        quotes: ['test quote'],
        maxQuotes: 10
      }
    },
    methods: {
      newQuote(quote) {
        this.quotes.push(quote);
      },
      deleteQuote(index) {
        this.quotes.splice(index, 1);
      }
    },
    components: {
      quoteGrid: QuoteGrid,
      newQuote: NewQuote,
    },
  }
</script>

<style>
</style>

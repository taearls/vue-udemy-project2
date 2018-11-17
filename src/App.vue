<template>
  <div class="container">
    <app-header></app-header>
    <create-quote></create-quote>
    <quote-grid></quote-grid>
    <app-footer></app-footer>
  </div>
</template>

<script>
  import Footer from './components/shared/Footer.vue';
  import Header from './components/shared/Header.vue';

  import CreateQuote from './components/Quotes/CreateQuote.vue';
  import QuoteGrid from './components/Quotes/QuoteGrid.vue';
  import Quote from './components/Quotes/Quote.vue';

  export default {
    data: () => {
      return {
        quotes: [],
        maxQuotes: 10
      }
    },
    components: {
      appFooter: Footer,
      appHeader: Header,
      quoteGrid: QuoteGrid,
      createQuote: CreateQuote,
      quote: Quote
    },
  }
</script>

<style>
</style>

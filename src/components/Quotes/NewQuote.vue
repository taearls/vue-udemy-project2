<template>
  <div class="row text-center">
    <form>          
      <label>Quote</label>
      <textarea class="form-control" rows="3" v-model="quote"></textarea>
    </form>
    <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group">
      <button class="btn btn-lg btn-primary" @click.prevent="createNew">Add Quote</button>
    </div>
  </div>
</template>

<script>
  export default {
    data: () => {
      return {
        quote: ''
      }
    },
    methods: {
      createNew() {
        this.$emit('quoteAdded', this.quote);
        this.quote = ''
      }
    }
  }
</script>

<style>

</style>
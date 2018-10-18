<template>
    <div class="row">
      <div class="col-sm-8 col-md-6 mx-auto">
        <form action="">
          <div class="form-group">
            <label>Quote:</label>
            <textarea rows="3" class="form-control" v-model="quote"></textarea>
          </div>
          <div class="form-group">
            <button class="btn btn-primary" @click.prevent="createNew">Add Quote</button>
          </div>
        </form>
      </div>
    </div>
</template>

<script>
    export default {
        name: "NewQuote",
      data() {
          return {
            quote:''
          }
      },
      methods: {
        createNew() {
          this.$emit('quoteAdded', this.quote);
          this.quote = '';
        }
      }
    }
</script>

<style>

</style>

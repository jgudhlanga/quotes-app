<template>
    <div class="row my-3">
       <div class="col-sm-12">
         <h3>Quotes Added</h3>
         <div class="progress">
           <div class="progress-bar" role="progressbar" :style="barWidth" aria-valuenow="0" aria-valuemin="0" aria-valuemax="100">
              {{ quotesCount }} / {{ maxQuotes }}
           </div>
         </div>
       </div>
      <hr>
    </div>
</template>
<script>
  export default {
    props: ['quotesCount', 'maxQuotes'],
    computed: {
      barWidth() {
        return {
          width: (this.quotesCount / this.maxQuotes) * 100 + '%'
        }
      }
    }
  }
</script>


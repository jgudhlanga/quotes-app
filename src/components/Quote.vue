<template>
    <div class="col-sm-6 col-md-4 col-lg-3 mt-3">
        <div class="card">
          <div class="card-body quote">
              <slot></slot>
          </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Quote",
    }
</script>

<style scoped>
    .card-body {
      font-family: 'Arizonia', cursive;
      font-size: 24px;
      color: #6e6e6e;
    }
  .quote {
    cursor: pointer;
  }
  .quote:hover {
      background-color: #ffe2e2;
  }
  .card {
    min-height: 150px !important;
  }
</style>

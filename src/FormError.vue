<template>
  <div v-if="errors" class="has-error">
    <slot></slot>
    <p v-for="error in errors" class="error-message">
      {{error}}
    </p>
  </div>
  <div v-else>
    <slot></slot>
  </div>

</template>

<script>
    export default {
        props: ['errors'],
    }
</script>

<style>
  .has-error {
    color: #ff4941;
  }
  .has-error input,.has-error select{
    border-color: red;
  }
  .has-error .error-message{
    text-align: center;
    color: #ff4941;
  }
</style>

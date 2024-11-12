<script>
export default {
    data() {
      return {
        count: 1
      }
    },
    methods: {
        incrementCount() {
            this.count++;
        }
    }
}
</script>

<template>
  <div>
    <div>Not Shared</div>
    <button v-on:click="incrementCount">Current Count is: {{ count }}</button>
  </div>
</template>
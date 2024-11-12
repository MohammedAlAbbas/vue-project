<script>
export default {
    props: {
        count: {
            type: Number,
            required: true
        },
        countButtonText: String
    }, // or ['count', 'countButtonText'],
    emits: ['clickSharedCountButton'] //$emit('clickSharedCountButton')
}
</script>

<template>
  <div>
    <div>Shared: </div>
    <button v-on:click="$emit('clickSharedCountButton')">{{countButtonText}} {{ count }}</button>
  </div>
</template>
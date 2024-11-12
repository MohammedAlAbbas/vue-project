<script>
import Counter from '../components/Counter.vue';
import CounterSharedState from '@/components/CounterSharedState.vue';

export default {
    components: {
        Counter,
        CounterSharedState
    },
    data() {
      return {
        count: 1
      }
    },
    methods: {
        incrementCount() {
            console.log('increment count');
            this.count++;
        }
    }
}
</script>

<template>
    <div>Buttons with their own count</div>
    <div>
        <Counter/>
    <Counter/>
    <Counter/>
    </div>
    
    <div>
        <div>Buttons With Shared Count</div>
        <CounterSharedState
     v-on:clickSharedCountButton="incrementCount"
     v-bind:count="count"
     countButtonText="Shared Count is: "/>
     <CounterSharedState
     v-on:clickSharedCountButton="incrementCount"
     v-bind:count="count"
     countButtonText="Shared Count is: "/>
     <CounterSharedState
     v-on:clickSharedCountButton="incrementCount"
     v-bind:count="count"
     count-button-text="Shared Count is: "/>

    </div>


</template>
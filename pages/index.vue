<template>
    <div>
      <h1>Welcome to the homepage</h1>
      <AppAlert>
        This is an auto-imported component
      </AppAlert>
      <div>this is global count: {{ globalCount }}</div>
      <Counter name="counter component"  @update-global-count="increment"/>
    </div>
</template>

<script>
import Counter from '../components/Counter.vue'

export default {
  components: {
    Counter
  },
  data: () => ({
      globalCount:0
  }),
  methods:{
    increment(){
      this.globalCount++
    }
  }
}
</script>
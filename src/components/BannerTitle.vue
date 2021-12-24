<template>
  <h1>{{ text }}</h1>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  props: {
    text: {
      type: [String],
      require: true
    }
  }
})
</script>

<style scoped>
h1 {
  font-family: 'Righteous', sans-serif;
  font-size: 64px;
  color: #fff2e7;
  margin: 0;
}

@media screen and (max-width: 425px) {
  h1 {
    
    font-size: 40px;
    
  }
}
</style>

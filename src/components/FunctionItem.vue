<template>
  <p>{{text}}</p>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  props: {
    text: {
      type: String,
      require: true
    }
  }
})
</script>

<style scoped>
  p{
    font-family: 'Sarala', sans-serif;
    font-weight: 300;
    color: #ECD6C4;
  }

  @media screen and (max-width: 425px) {
  p {
    
    font-size: .7rem;
    
  }
}
</style>

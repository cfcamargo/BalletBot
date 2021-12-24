<template>
  <p>{{ text }}</p>
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
p {
  font-family: "Sarala", sans-serif;
  font-size: 1.2rem;
  color: #FFF2E7;
  width: 100%;
}

@media screen and (max-width: 906px) {
  p{
    text-align: center;
  }
}

@media screen and (max-width: 425px) {
  p {
    
    font-size: .7rem;
    
  }
}

</style>
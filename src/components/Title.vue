<template>
  <h2 class="title-secondary">{{ text }}</h2>
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
h2 {
  font-family: Righteous;
  color: #fff2e7;
  font-weight: normal;
  font-size: 24px;
  margin-top: 2rem;
}
</style>

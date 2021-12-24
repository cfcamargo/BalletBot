<template>
  <button>
    {{ text }}
  </button>
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
button {
  width: 185px;
  height: 50px;
  padding: 14px 45px;
  border-radius: 20px;
  background-color: #ecd6c4;
  box-shadow: 4px 5px 4px rgba(0, 0, 0, 0.25);
  border: none;
  font-family: 'Sarala', sans-serif;
  color: #2F2325;
  cursor: pointer;
  margin-top: 3rem;
}

button:hover{
  transform: scale(1.03);
}
</style>

<template>
 <div class="header">
    <Header />
 </div>
    
  
</template>

<script lang="ts">
import { defineComponent } from "vue";
import Header from "@/components/Header.vue"


export default defineComponent({
  components: { Header }
});
</script>

<style>
.header{
  border-bottom: 0.4px solid #fff2e7;
  width: 100%;
}
</style>

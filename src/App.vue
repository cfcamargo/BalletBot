<template>
  <div class="layout">
    <div class="header">
      <Header />
    </div>

    <div class="main">
      <Home />
    </div>
    <div class="footer">
      <Footer />
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import Header from '@/components/Header.vue'
import Home from '@/components/Home.vue'
import Footer from '@/components/Footer.vue'

export default defineComponent({
  components: { Header, Home, Footer }
})
</script>

<style>
.layout {
  height: 100%;
  width: 100%;
  display: grid;
  grid-template-columns: 100%;
  grid-template-rows: auto 1fr auto;
  grid-template-areas:
    'header'
    'main'
    'footer';
}

.header {
  border-bottom: 0.4px solid #fff2e7;
  grid-area: header;
}

.main{
  grid-area: main;
  display: flex;
  justify-content: center;
  align-items: center;
}

.footer {
  grid-area: footer;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  padding: 1rem 0;
  border-top: 0.4px solid #fff2e7;
}
</style>

<template>
  <div class="container">
      <div class="nav-menu">
    <LogoHeader />
    <NavMenu />
  </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import LogoHeader from '@/components/LogoHeader.vue'
import NavMenu from '@/components/NavMenu.vue'

export default defineComponent({
  components: { LogoHeader, NavMenu }
})
</script>

<style scoped>
.container {
  max-width: 990px;
  width: 90%;
  margin: 0 auto;
}

.nav-menu {
  padding: 18px 0;
  display: grid;
  grid-template-columns: 70px 1fr;
  justify-content: space-between;
  align-items: center;
  
}
</style>

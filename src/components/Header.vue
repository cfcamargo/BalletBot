<template>
  <Container>
    <div class="nav-menu">
      <LogoHeader />
      <NavMenu />
    </div>
  </Container>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import LogoHeader from '@/components/LogoHeader.vue'
import NavMenu from '@/components/NavMenu.vue'
import Container from '@/components/Container.vue'

export default defineComponent({
  components: { LogoHeader, NavMenu, Container }
})
</script>

<style scoped>
.container {
  max-width: 990px;
  width: 90%;
  margin: 0 auto;
}

.logo-menu {
  grid-area: logo;
}

.nav-menu {
  padding: 18px 0;
  display: grid;
  grid-template-columns: 70px 1fr;
  grid-template-areas: 'logo menu';
  justify-content: space-between;
  align-items: center;
}
</style>

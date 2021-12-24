<template>
  <nav id="menu-principal">
    <NavLink text="Comunidade Ballerini" />
    <NavLink text="Tutorial" />
    <NavLink text="Open Source" />
    <NavLink text="Comandos" />
  </nav>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import NavLink from '@/components/NavLinks.vue'

export default defineComponent({
  components: { NavLink }
})
</script>

<style scoped>
#menu-principal {
  display: flex;
  gap: 0.5rem;
  justify-content: flex-end;
}
</style>

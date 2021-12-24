<template>
  <div id="menu-mobile" @click="showMenu()">
    <i class="fas fa-bars"></i>
  </div>

  <transition
    enter-active-class="aanimate__animated animate__slideInLeft"
    leave-active-class="animate__animated animate__slideOutLeft"
  >
    <nav id="menu-principal" :class="{ isMobile: isActive }">
      <NavLink text="Comunidade Ballerini" />
      <NavLink text="Tutorial" />
      <NavLink text="Open Source" />
      <NavLink text="Comandos" />
    </nav>
  </transition>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import '@fortawesome/fontawesome-free/css/all.css'
import NavLink from '@/components/NavLinks.vue'
import 'animate.css'

export default defineComponent({
  components: { NavLink },
  data() {
    var isActive = false
    return {
      isActive
    }
  },
  methods: {
    showMenu() {
      this.isActive = !this.isActive
      console.log('Menu Aberto')
    }
  }
})
</script>

<style scoped>
#menu-principal {
  display: flex;
  gap: 0.5rem;
  justify-content: flex-end;
}

#menu-mobile i {
  font-size: 2.5rem;
  color: white;
}

#menu-mobile {
  display: none;
}

.isMobile {
  width: 70%;
  height: 100%;
  position: absolute;
  top: 0;
  left: 0;
  background-color: #2f2325;
  flex-direction: column;
  align-items: flex-start;
  justify-content: center !important;
  gap: 5rem !important;
  transition: all ease 0.3s;
}

@media screen and (max-width: 768px) {
  #menu-principal {
    display: none;
  }

  .isMobile {
    display: flex !important;
  }

  #menu-mobile {
    display: grid;
    cursor: pointer;
    justify-content: flex-end;
  }
}
</style>

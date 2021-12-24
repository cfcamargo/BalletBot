<template>
  <FunctionItem text="1. Cria um sistema de verificação capcha para novos membros garantirem que não são robos"/>
  <FunctionItem text="2. Possui um sistema de banimento automático para links suspeitos que forem enviados na comunidade"/>
  <FunctionItem text="3. Sistema de avisos e banimento manual, para pessoas administradoras utilizarem"/>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import FunctionItem from '@/components/FunctionItem.vue'

export default defineComponent({
  components: { FunctionItem }
})
</script>

<style scoped></style>

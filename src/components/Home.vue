<template>
  <Container>
    <div class="layout">
      <div class="banner">
        <div class="banner-content">
          <BannerTitle text="Balle Bot" />
          <BannerDescription
            text="Deixe a sua comunidade segura de um jeito fácil"
          />
          <ActionButton text="Me Adicione!" />
        </div>
        <div class="banner-image"><BannerImage /></div>
      </div>
      <div class="divisor-line">
        <Divisor />
      </div>

      <div class="description">
        <Container>
          <Title text="O que ela faz por você?" />
          <ListFunctions />
        </Container>
      </div>
    </div>
  </Container>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import Container from '@/components/Container.vue'
import Divisor from '@/components/Divisor.vue'
import BannerTitle from '@/components/BannerTitle.vue'
import BannerDescription from '@/components/BannerDescription.vue'
import ActionButton from '@/components/ActionButton.vue'
import BannerImage from '@/components/BallebotAvatar.vue'
import Title from './Title.vue'
import ListFunctions from '@/components/ListFunctions.vue'

export default defineComponent({
  components: {
    Container,
    Divisor,
    BannerTitle,
    BannerDescription,
    ActionButton,
    BannerImage,
    Title,
    ListFunctions
  }
})
</script>

<style scoped>
.layout {
  padding: 1rem 0;
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: 1.5fr auto auto;
  gap: 1rem;
  grid-template-areas:
    'banner'
    'divisor'
    'description';
}

.banner {
  grid-area: 'banner';
  width: 100%;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 1rem;
  justify-content: center;
}

.banner-content {
  display: flex;
  width: 100%;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
}

.banner-image {
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.avatar {
  width: 350px;
}

.divisor-line {
  grid-area: 'divisor';
  width: 100%;
}

.description {
  grid-area: 'description';
  width: 100%;
  text-align: center;
  margin: 0;
  pad: 0;
}

@media screen and (max-width: 906px) {
  .banner-content {
    align-items: center;
  }
}

@media screen and (max-width: 425px) {
  .avatar{
    width: 250px;
  }
}
</style>

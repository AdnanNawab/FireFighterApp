<template>
  <div>
    <NavBar />
    <div class="container">
      <TheHero /><br /><br /><br />

      <LargeCardDisplay
        v-for="cardInfo in largeCardInfo"
        :key="cardInfo.id"
        :cardsSection="cardInfo"
      />
      <SmallCardDisplay
        v-for="cardInfo in smallCardSections"
        :key="cardInfo.id"
        :cardsSection="cardInfo"
      />
    </div>
  </div>
</template>

<script>
import { largeCardSections, smallCardSections } from '@/assets/data.js'
import TheHero from '~/components/TheHero.vue'
import LargeCardDisplay from '~/components/LargeCardDisplay.vue'
import SmallCardDisplay from '~/components/SmallCardDisplay.vue'
import NavBar from '../components/NavBar.vue'
export default {
  data() {
    return {
      largeCardInfo: largeCardSections,
      smallCardSections,
    }
  },
  name: 'IndexPage',
  components: { TheHero, LargeCardDisplay, SmallCardDisplay, NavBar },
}
</script>


<!-- <style scoped>
.nav {
  align-content: center;
} -->
</style>

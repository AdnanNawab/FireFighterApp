<template>
  <div>
    <NavBar />

    <div class="container">
      <LargeCardDisplay
        v-for="cardInfo in largeCardInfo.slice(0, 1)"
        :key="cardInfo.id"
        :cardsSection="cardInfo"
      />
      <SmallCardDisplay
        v-for="cardInfo in smallCardsSection"
        :key="cardInfo.id"
        :cardsSection="cardInfo"
      />
    </div>
  </div>
</template>

<script>
import { largeCardSections, smallCardSections } from '~/assets/data'
import LargeCardDisplay from '~/components/LargeCardDisplay.vue'
import SmallCardDisplay from '~/components/SmallCardDisplay.vue'
import NavBar from '~/components/NavBar.vue'
export default {
  data() {
    return {
      largeCardInfo: largeCardSections,
      smallCardsSection: smallCardSections,
    }
  },
  components: { LargeCardDisplay, SmallCardDisplay, NavBar },
}
</script>

<style>
</style>
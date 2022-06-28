<template>
  <div class="flex flex-col items-center align-center justify-center">
    <PricingHeader />
    <template v-for="(pricing, idx) in cards.reverse()" >
      <PricingCard :key="idx" :pricing="pricing" class="mt-5" />
    </template>
  </div>
</template>

<script>
import PricingCard from '../components/pricingComponents/PricingCard.vue'
import PricingHeader from '../components/pricingComponents/PricingHeader.vue'
export default {
    components: [PricingCard, PricingHeader],
    layout: 'default',
    data: () => ({
    cards: [
      {
        title: '1% of each sale',
        recommended: true,
      }
      ,]
} )
}
</script>

<style>

</style>
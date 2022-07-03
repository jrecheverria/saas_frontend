<template>
  <div
    class="bg-white rounded-xl p-2 sm:p-6 md:p-8 lg:p-12 shadow-xl w-1/4"
    :class="
      pricing.recommended
        ? 'border-4 border-green-500	'
        : 'border border-slate-100'
    "
  >
    
    <h2 class="font-bold text-2xl">{{ pricing.title }}</h2>
    <div class="font-regular text-lg mt-3 tracking-wide">

      <a href="https://stripe.com/pricing" class="text-blue-500">Plus Stripe Payment Processing Fees</a>
    </div>

    
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  name: 'PricingCard',
  props: {
    pricing: {
      type: Object,
      default: () => ({}),
      required: true,
    },
  },
})
</script>

<style></style>
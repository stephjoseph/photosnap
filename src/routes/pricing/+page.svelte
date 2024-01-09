<script>
  import PricingFeatures from '../../lib/pricing/pricing-features.svelte';
  import PricingHero from '../../lib/pricing/pricing-hero.svelte';
  import PricingPlans from '../../lib/pricing/pricing-plans.svelte';
  import Cta from '../../lib/shared/cta.svelte';
</script>

<svelte:head>
  <title>Photosnap - Pricing</title>
</svelte:head>
<main class="mt-[7.5rem] md:mt-0">
  <PricingHero />
  <PricingPlans />
  <PricingFeatures />
  <Cta />
</main>

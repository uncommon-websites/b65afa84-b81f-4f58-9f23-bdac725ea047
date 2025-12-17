<script lang="ts">
	import Navbar from '$lib/components/Navbar.svelte';
	import Hero from '$lib/components/Hero.svelte';
	import FeaturesGrid from '$lib/components/FeaturesGrid.svelte';
	import ChartSection from '$lib/components/ChartSection.svelte';
	import PricingSection from '$lib/components/PricingSection.svelte';
	import FeatureBlocks from '$lib/components/FeatureBlocks.svelte';
	import UpdatesSection from '$lib/components/UpdatesSection.svelte';
	import Footer from '$lib/components/Footer.svelte';
</script>

<main class="min-h-screen bg-background text-foreground selection:bg-accent/20">
	<Navbar />
	<Hero />
	<FeaturesGrid />
	<ChartSection />
	<PricingSection />
	<FeatureBlocks />
	<UpdatesSection />
	<Footer />
</main>


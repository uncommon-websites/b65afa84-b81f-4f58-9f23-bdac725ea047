<script lang="ts">
	// Pricing tiers
	const tiers = [
		{ requests: 10_000_000, price: 500, label: '10M' },
		{ requests: 50_000_000, price: 1500, label: '50M' },
		{ requests: 100_000_000, price: 3000, label: '100M' },
		{ requests: 250_000_000, price: 6000, label: '250M' },
		{ requests: 500_000_000, price: 10000, label: '500M' }
	];

	let sliderValue = $state(2); // Default to 100M

	let currentTier = $derived(tiers[sliderValue]);
	let costPer1k = $derived((currentTier.price / (currentTier.requests / 1000)).toFixed(3));
	let savings = $derived(sliderValue > 0
		? Math.round((1 - (currentTier.price / currentTier.requests) / (tiers[0].price / tiers[0].requests)) * 100)
		: 0
	);
	let fillPercent = $derived((sliderValue / 4) * 100);
</script>

<section class="py-20 border-b border-border">
	<div class="container-custom">
		<!-- Header -->
		<div class="flex flex-col md:flex-row justify-between items-start mb-16 gap-8">
			<div>
				<p class="font-mono text-xs text-muted mb-4">Transparent pricing</p>
				<h2 class="text-3xl font-medium mb-2">Pay for what you protect</h2>
				<p class="text-xl text-muted font-light">Volume discounts that scale with your traffic</p>
			</div>
			<div class="max-w-xs text-[10px] text-muted leading-relaxed border-l border-border pl-4">
				<strong class="text-foreground block mb-1">No hidden fees</strong>
				All plans include full bot detection, real-time dashboard, crawler management, and dedicated support. No setup costs or long-term contracts required.
			</div>
		</div>

		<!-- Calculator Card -->
		<div class="grid grid-cols-1 lg:grid-cols-5 gap-8">

			<!-- Slider Section -->
			<div class="lg:col-span-3 bg-white border border-border rounded-sm p-8">
				<div class="mb-8">
					<label class="font-mono text-xs text-muted block mb-6">MONTHLY REQUESTS</label>

					<!-- Custom Slider -->
					<div class="relative pb-10">
						<input
							type="range"
							min="0"
							max="4"
							step="1"
							bind:value={sliderValue}
							class="pricing-slider"
							style="--fill: {fillPercent}%"
						/>

						<!-- Tick marks and labels -->
						<div class="flex justify-between mt-4">
							{#each tiers as tier, idx}
								<button
									class="flex flex-col items-center"
									onclick={() => sliderValue = idx}
								>
									<span class="w-0.5 h-2 {idx <= sliderValue ? 'bg-accent' : 'bg-gray-300'} mb-1 rounded-full"></span>
									<span class="font-mono text-[10px] {sliderValue === idx ? 'text-accent font-medium' : 'text-muted'}">{tier.label}</span>
								</button>
							{/each}
						</div>
					</div>
				</div>

				<!-- Visual indicator -->
				<div class="bg-primary-50 border border-border rounded-sm p-4 mb-6">
					<div class="flex items-center justify-between mb-3">
						<span class="font-mono text-[10px] text-muted">REQUESTS PROTECTED</span>
						<span class="font-mono text-[10px] text-muted">COST PER 1K</span>
					</div>
					<div class="flex items-center justify-between">
						<span class="text-2xl font-medium">{currentTier.label}<span class="text-muted font-light">/mo</span></span>
						<span class="font-mono text-sm text-accent">${costPer1k}</span>
					</div>
				</div>

				<!-- Included features -->
				<div class="grid grid-cols-2 gap-3">
					{#each [
						'Full bot detection',
						'Real-time dashboard',
						'Crawler management',
						'API access',
						'GDPR compliant',
						'Priority support'
					] as feature}
						<div class="flex items-center gap-2 text-xs text-muted">
							<svg class="w-3 h-3 text-accent" viewBox="0 0 12 12" fill="none">
								<path d="M2 6L5 9L10 3" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
							</svg>
							{feature}
						</div>
					{/each}
				</div>
			</div>

			<!-- Price Display -->
			<div class="lg:col-span-2 bg-white border border-border rounded-sm p-8 flex flex-col">
				<div class="font-mono text-xs text-muted mb-2">MONTHLY COST</div>

				<div class="mb-6">
					<span class="text-5xl font-medium tracking-tight">${currentTier.price.toLocaleString()}</span>
					<span class="text-muted font-light">/month</span>
				</div>

				{#if savings > 0}
					<div class="inline-flex items-center gap-2 bg-accent/10 text-accent px-2 py-1 rounded text-xs font-mono mb-6 w-fit">
						<svg class="w-3 h-3" viewBox="0 0 12 12" fill="none">
							<path d="M6 9V3M6 3L3 6M6 3L9 6" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
						</svg>
						{savings}% savings vs base rate
					</div>
				{/if}

				<div class="space-y-3 mb-8 flex-1">
					<div class="flex justify-between text-xs">
						<span class="text-muted">Base rate (10M)</span>
						<span class="font-mono">$0.050/1k</span>
					</div>
					<div class="flex justify-between text-xs">
						<span class="text-muted">Your rate ({currentTier.label})</span>
						<span class="font-mono text-accent">${costPer1k}/1k</span>
					</div>
					<div class="border-t border-border pt-3 flex justify-between text-xs">
						<span class="text-muted">Annual (billed monthly)</span>
						<span class="font-mono">${(currentTier.price * 12).toLocaleString()}</span>
					</div>
				</div>

				<div class="space-y-3 mt-auto">
					<button class="w-full bg-foreground text-background py-3 text-xs font-mono uppercase hover:bg-foreground/90 transition-colors">
						Start Free Trial
					</button>
					<button class="w-full border border-border py-3 text-xs font-mono uppercase hover:bg-primary-50 transition-colors flex items-center justify-center gap-2">
						Request Custom Quote
						<svg width="12" height="12" viewBox="0 0 12 12" fill="none">
							<path d="M1 11L11 1M11 1H3M11 1V9" stroke="currentColor" stroke-width="1.5"/>
						</svg>
					</button>
				</div>
			</div>
		</div>

		<!-- Enterprise callout -->
		<div class="mt-8 bg-gray-50 border border-border rounded-sm p-6 flex flex-col md:flex-row items-start md:items-center justify-between gap-4">
			<div class="flex items-start gap-4">
				<div class="w-10 h-10 bg-white border border-border rounded-sm flex items-center justify-center shrink-0">
					<svg class="w-5 h-5 text-muted" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
						<path d="M19 21V5a2 2 0 00-2-2H7a2 2 0 00-2 2v16m14 0h2m-2 0h-5m-9 0H3m2 0h5M9 7h1m-1 4h1m4-4h1m-1 4h1m-5 10v-5a1 1 0 011-1h2a1 1 0 011 1v5m-4 0h4"/>
					</svg>
				</div>
				<div>
					<div class="font-medium text-sm mb-1">Enterprise & High-Volume</div>
					<p class="text-xs text-muted">Processing 500M+ requests? Get custom pricing, dedicated infrastructure, SLA guarantees, and a named account manager.</p>
				</div>
			</div>
			<button class="shrink-0 border border-border px-4 py-2 text-xs font-mono uppercase hover:bg-white transition-colors">
				Contact Sales
			</button>
		</div>
	</div>
</section>

<style>
	.pricing-slider {
		-webkit-appearance: none;
		appearance: none;
		background: transparent;
		cursor: pointer;
		width: 100%;
		height: 24px;
	}

	.pricing-slider:focus {
		outline: none;
	}

	/* Chrome, Safari, Opera, Edge Chromium */
	.pricing-slider::-webkit-slider-runnable-track {
		height: 8px;
		border-radius: 9999px;
		background: linear-gradient(
			to right,
			#3b82f6 0%,
			#3b82f6 var(--fill, 50%),
			#e5e7eb var(--fill, 50%),
			#e5e7eb 100%
		);
	}

	.pricing-slider::-webkit-slider-thumb {
		-webkit-appearance: none;
		appearance: none;
		width: 24px;
		height: 24px;
		background: white;
		border: 3px solid #3b82f6;
		border-radius: 50%;
		box-shadow: 0 2px 6px rgba(0, 0, 0, 0.15);
		margin-top: -8px;
		transition: box-shadow 0.15s ease;
	}

	.pricing-slider::-webkit-slider-thumb:hover {
		box-shadow: 0 3px 10px rgba(59, 130, 246, 0.3);
	}

	.pricing-slider:focus::-webkit-slider-thumb {
		box-shadow: 0 0 0 4px rgba(59, 130, 246, 0.2), 0 2px 6px rgba(0, 0, 0, 0.15);
	}

	/* Firefox */
	.pricing-slider::-moz-range-track {
		height: 8px;
		border-radius: 9999px;
		background: #e5e7eb;
	}

	.pricing-slider::-moz-range-progress {
		height: 8px;
		border-radius: 9999px;
		background: #3b82f6;
	}

	.pricing-slider::-moz-range-thumb {
		width: 24px;
		height: 24px;
		background: white;
		border: 3px solid #3b82f6;
		border-radius: 50%;
		box-shadow: 0 2px 6px rgba(0, 0, 0, 0.15);
	}

	.pricing-slider:focus::-moz-range-thumb {
		box-shadow: 0 0 0 4px rgba(59, 130, 246, 0.2), 0 2px 6px rgba(0, 0, 0, 0.15);
	}
</style>

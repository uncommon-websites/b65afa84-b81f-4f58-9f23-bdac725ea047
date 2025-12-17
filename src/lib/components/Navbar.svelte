<script lang="ts">
	let showBanner = $state(true);
	let mobileMenuOpen = $state(false);
</script>

{#if showBanner}
	<div class="bg-primary-50 border-b border-border py-2 px-4 text-xs font-mono flex justify-center items-center relative">
		<div class="flex items-center gap-2">
			<span class="text-muted">GDPR-compliant bot protection. Fully hosted in Germany.</span>
			<a href="#" class="underline decoration-muted hover:text-accent transition-colors">Learn more.</a>
		</div>
		<button
			class="absolute right-4 text-muted hover:text-foreground"
			aria-label="Close banner"
			onclick={() => showBanner = false}
		>
			<svg width="12" height="12" viewBox="0 0 12 12" fill="none" xmlns="http://www.w3.org/2000/svg">
				<path d="M9 3L3 9M3 3L9 9" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
			</svg>
		</button>
	</div>
{/if}

<nav class="border-b border-border bg-background sticky top-0 z-50">
	<div class="container-custom h-16 flex items-center justify-between">
		<!-- Logo -->
		<a href="/" class="text-xl font-bold tracking-tight flex items-center gap-2">
			<svg xmlns="http://www.w3.org/2000/svg" width="28" height="28" viewBox="0 0 48 48">
				<circle cx="24" cy="24" r="24" fill="#3B82F6" opacity="0.3"/>
				<circle cx="24" cy="24" r="16" fill="#3B82F6"/>
				<circle cx="24" cy="24" r="8" fill="white"/>
			</svg>
			<span class="font-sans font-semibold">Centinel Analytica</span>
		</a>

		<!-- Links -->
		<div class="hidden md:flex items-center gap-8 font-mono text-xs text-muted">
			<a href="#" class="hover:text-foreground transition-colors">Product</a>
			<a href="#" class="hover:text-foreground transition-colors">Solutions</a>
			<a href="#" class="hover:text-foreground transition-colors">Pricing</a>
			<a href="#" class="hover:text-foreground transition-colors">Resources</a>
			<a href="#" class="hover:text-foreground transition-colors">Contact</a>
		</div>

		<!-- CTA -->
		<div class="flex items-center gap-4">
			<a href="#" class="hidden md:flex items-center gap-2 border border-border px-3 py-1.5 text-xs font-mono hover:bg-primary-50 transition-colors uppercase">
				Request Demo
				<svg width="12" height="12" viewBox="0 0 12 12" fill="none" xmlns="http://www.w3.org/2000/svg">
					<path d="M1 11L11 1M11 1H3M11 1V9" stroke="currentColor" stroke-width="1.5"/>
				</svg>
			</a>
			<button
				class="md:hidden p-1"
				onclick={() => mobileMenuOpen = !mobileMenuOpen}
				aria-label="Toggle menu"
			>
				{#if mobileMenuOpen}
					<svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
						<path d="M18 6L6 18M6 6l12 12"/>
					</svg>
				{:else}
					<svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
						<line x1="3" y1="12" x2="21" y2="12"></line>
						<line x1="3" y1="6" x2="21" y2="6"></line>
						<line x1="3" y1="18" x2="21" y2="18"></line>
					</svg>
				{/if}
			</button>
		</div>
	</div>

	<!-- Mobile Menu -->
	{#if mobileMenuOpen}
		<div class="md:hidden border-t border-border bg-background">
			<div class="container-custom py-4 flex flex-col gap-4">
				<a href="#" class="py-2 text-sm hover:text-accent transition-colors" onclick={() => mobileMenuOpen = false}>Product</a>
				<a href="#" class="py-2 text-sm hover:text-accent transition-colors" onclick={() => mobileMenuOpen = false}>Solutions</a>
				<a href="#" class="py-2 text-sm hover:text-accent transition-colors" onclick={() => mobileMenuOpen = false}>Pricing</a>
				<a href="#" class="py-2 text-sm hover:text-accent transition-colors" onclick={() => mobileMenuOpen = false}>Resources</a>
				<a href="#" class="py-2 text-sm hover:text-accent transition-colors" onclick={() => mobileMenuOpen = false}>Contact</a>
				<div class="pt-4 border-t border-border">
					<a href="#" class="inline-flex items-center gap-2 bg-foreground text-background px-4 py-2 text-xs font-mono uppercase">
						Request Demo
						<svg width="12" height="12" viewBox="0 0 12 12" fill="none" xmlns="http://www.w3.org/2000/svg">
							<path d="M1 11L11 1M11 1H3M11 1V9" stroke="currentColor" stroke-width="1.5"/>
						</svg>
					</a>
				</div>
			</div>
		</div>
	{/if}
</nav>

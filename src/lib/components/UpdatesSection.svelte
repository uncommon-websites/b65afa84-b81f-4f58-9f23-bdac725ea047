<section class="py-20 border-b border-border">
	<div class="container-custom">
		<div class="grid grid-cols-1 md:grid-cols-2 gap-16">
			
			<!-- Left Column: CTA & Visual -->
			<div class="flex flex-col h-full">
				<div class="mb-8">
					<p class="font-mono text-xs text-muted mb-4">Start building</p>
					<h2 class="text-2xl font-medium mb-4">Towards a programmatic web for AIs</h2>
					<p class="text-muted font-light mb-8 text-sm leading-relaxed max-w-md">
						Parallel is building new interfaces, infrastructure, and business models for AIs to work with the web
					</p>
					<div class="flex gap-3 mb-12">
						<button class="border border-border px-3 py-1.5 text-xs font-mono uppercase hover:bg-primary-50 transition-colors flex items-center gap-2">
							TRY IT FOR FREE
							<span class="text-muted border border-muted/30 rounded px-1 text-[9px] min-w-[16px] text-center">P</span>
						</button>
						<button class="border border-border px-3 py-1.5 text-xs font-mono uppercase hover:bg-primary-50 transition-colors flex items-center gap-2">
							JOIN US
							<span class="text-muted border border-muted/30 rounded px-1 text-[9px] min-w-[16px] text-center">J</span>
						</button>
					</div>
				</div>
				
				<!-- Barcode Visual -->
				<div class="mt-auto w-full h-48 bg-black relative overflow-hidden flex items-center justify-center">
					{#each Array(100) as _, i}
						<div 
							class="h-full bg-white absolute" 
							style="
								left: {i}%; 
								width: {Math.random() * 2}%; 
								opacity: {Math.random()};
							"
						></div>
					{/each}
					<div class="absolute inset-0 flex items-center justify-center">
						<div class="bg-black text-white font-mono text-[10px] px-2 py-1 z-10">
							parallel.web
						</div>
					</div>
				</div>
			</div>

			<!-- Right Column: Updates -->
			<div>
				<p class="font-mono text-xs text-muted mb-8">Latest updates</p>
				
				<div class="space-y-12">
					<!-- Update 1 -->
					<div class="flex gap-8 group">
						<div class="font-mono text-xs text-muted w-24 shrink-0 pt-1">January 15</div>
						<div>
							<h3 class="font-medium text-sm mb-2 group-hover:text-accent transition-colors cursor-pointer">Network-level detection now live</h3>
							<p class="text-xs text-muted leading-relaxed mb-3">
								Centinel's advanced network-level detection identifies stealth bots that evade traditional fingerprinting methods. This proprietary technology, built from 15+ years of scraper development expertise, detects 30% more threats than competing solutions while maintaining zero false positives for legitimate crawlers.
							</p>
							<span class="bg-gray-100 text-[10px] px-1.5 py-0.5 rounded text-muted">Product Release</span>
						</div>
					</div>

					<!-- Update 2 -->
					<div class="flex gap-8 group">
						<div class="font-mono text-xs text-muted w-24 shrink-0 pt-1">December 8</div>
						<div>
							<h3 class="font-medium text-sm mb-2 group-hover:text-accent transition-colors cursor-pointer">European publishers achieve 28% cost reduction</h3>
							<p class="text-xs text-muted leading-relaxed mb-3">
								Major European publishers report average 28% reduction in AWS and CDN costs within 60 days of deploying Centinel. By blocking bot traffic at the edge, publishers eliminate wasteful infrastructure spending while protecting premium content from AI scrapers.
							</p>
							<div class="flex gap-2">
								<span class="bg-gray-100 text-[10px] px-1.5 py-0.5 rounded text-muted">Case Study</span>
								<span class="bg-gray-100 text-[10px] px-1.5 py-0.5 rounded text-muted">ROI</span>
							</div>
						</div>
					</div>

					<!-- Update 3 -->
					<div class="flex gap-8 group">
						<div class="font-mono text-xs text-muted w-24 shrink-0 pt-1">November 22</div>
						<div>
							<h3 class="font-medium text-sm mb-2 group-hover:text-accent transition-colors cursor-pointer">GDPR-compliant bot protection for EU publishers</h3>
							<p class="text-xs text-muted leading-relaxed mb-3">
								Centinel launches fully German-hosted infrastructure, providing EU data sovereignty and GDPR compliance by design. European publishers can now protect their content without compromising on data privacy or regulatory requirements.
							</p>
							<span class="bg-gray-100 text-[10px] px-1.5 py-0.5 rounded text-muted">Product Release</span>
						</div>
					</div>

					<!-- Update 4 -->
					<div class="flex gap-8 group">
						<div class="font-mono text-xs text-muted w-24 shrink-0 pt-1">October 10</div>
						<div>
							<h3 class="font-medium text-sm mb-2 group-hover:text-accent transition-colors cursor-pointer">Centinel processes 500M+ requests monthly</h3>
							<p class="text-xs text-muted leading-relaxed mb-3">
								Centinel's platform now handles over 500 million requests per month across publisher clients, identifying an average of 24% bot traffic while maintaining zero SEO impact through intelligent crawler whitelisting.
							</p>
							<span class="bg-gray-100 text-[10px] px-1.5 py-0.5 rounded text-muted">Milestone</span>
						</div>
					</div>
				</div>
			</div>

		</div>
	</div>
</section>

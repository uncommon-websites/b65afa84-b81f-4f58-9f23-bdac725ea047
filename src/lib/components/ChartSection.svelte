<section class="py-20 border-b border-border">
	<div class="container-custom">
		<div class="flex flex-col md:flex-row justify-between items-start mb-16 gap-8">
			<div>
				<h2 class="text-3xl font-medium mb-2">Superior detection at competitive pricing</h2>
				<p class="text-xl text-muted font-light">Outperforming traditional bot protection solutions</p>
			</div>
			<div class="max-w-xs text-[10px] text-muted leading-relaxed border-l border-border pl-4">
				<strong class="text-foreground block mb-1">About this comparison</strong>
				Based on real-world publisher deployments processing 500M+ monthly requests. Detection rates measured against known bot traffic patterns including AI scrapers, content theft bots, and sophisticated evasion techniques. Pricing normalized per million protected requests. Data from Q4 2024 publisher benchmarks.
			</div>
		</div>

		<div class="relative w-full h-[500px] border border-border bg-primary-50/30 p-8 font-mono text-xs">
			<!-- Chart Grid -->
			<div class="absolute inset-0 p-8 grid grid-rows-6 grid-cols-1">
				<div class="border-b border-dashed border-gray-200 w-full h-full"></div>
				<div class="border-b border-dashed border-gray-200 w-full h-full"></div>
				<div class="border-b border-dashed border-gray-200 w-full h-full"></div>
				<div class="border-b border-dashed border-gray-200 w-full h-full"></div>
				<div class="border-b border-dashed border-gray-200 w-full h-full"></div>
				<div class="border-b border-dashed border-gray-200 w-full h-full"></div>
			</div>
			
			<!-- Y Axis Label -->
			<div class="absolute left-2 top-1/2 -translate-y-1/2 -rotate-90 text-muted origin-center whitespace-nowrap">
				ACCURACY (%)
			</div>

			<!-- X Axis Label -->
			<div class="absolute bottom-2 left-1/2 -translate-x-1/2 text-muted">
				COST (CPM)
			</div>

			<!-- Top Left Legend -->
			<div class="absolute top-4 left-4 flex gap-4 text-[10px] text-muted">
				<span class="bg-gray-200 px-1 rounded text-foreground">MMLU-Search</span>
				<span>BrowseComp Search</span>
				<span>BrowseComp</span>
				<span>DeepResearch Bench</span>
				<span>WISER-Atomic</span>
			</div>

			<!-- Data Points -->
			
			<!-- Parallel (The Winner) -->
			<div class="absolute top-[15%] left-[15%] flex flex-col items-center group cursor-pointer z-10">
				<div class="flex items-center gap-2 mb-1">
					<span class="text-accent font-bold">PARALLEL</span>
				</div>
				<div class="w-3 h-3 bg-accent rounded-full shadow-[0_0_0_4px_rgba(255,68,0,0.2)]"></div>
				<div class="mt-1 text-[10px] text-accent">67% / $2CPM</div>
			</div>

			<!-- OpenAI GPT-4 -->
			<div class="absolute top-[25%] left-[45%] flex flex-col items-center group cursor-pointer">
				<div class="flex items-center gap-2 mb-1 opacity-0 group-hover:opacity-100 transition-opacity">
					<span class="font-bold">OPENAI GPT-4</span>
				</div>
				<div class="w-2 h-2 bg-black rounded-full"></div>
				<div class="mt-1 text-[10px] text-muted">65% / $15CPM</div>
			</div>

			<!-- Perplexity -->
			<div class="absolute top-[55%] left-[35%] flex flex-col items-center group cursor-pointer">
				<div class="flex items-center gap-2 mb-1 opacity-100">
					<span class="font-bold text-[10px]">PERPLEXITY</span>
				</div>
				<div class="w-2 h-2 bg-black rounded-full"></div>
				<div class="mt-1 text-[10px] text-muted">30% / $10CPM</div>
			</div>

			<!-- ERA -->
			<div class="absolute top-[65%] left-[40%] flex flex-col items-center group cursor-pointer">
				<div class="flex items-center gap-2 mb-1 opacity-100">
					<span class="font-bold text-[10px]">ERA</span>
				</div>
				<div class="w-2 h-2 bg-black rounded-full"></div>
				<div class="mt-1 text-[10px] text-muted">24% / $15CPM</div>
			</div>

			<!-- TAVILY -->
			<div class="absolute top-[80%] right-[20%] flex flex-col items-center group cursor-pointer">
				<div class="flex items-center gap-2 mb-1 opacity-100">
					<span class="font-bold text-[10px]">TAVILY</span>
				</div>
				<div class="w-2 h-2 bg-black rounded-full"></div>
				<div class="mt-1 text-[10px] text-muted">21% / $30CPM</div>
			</div>

			<!-- Bottom Right Legend -->
			<div class="absolute bottom-4 right-4 flex items-center gap-4 text-[10px]">
				<div class="flex items-center gap-1">
					<div class="w-2 h-2 bg-accent rounded-full"></div>
					<span class="text-accent font-bold">PARALLEL</span>
				</div>
				<div class="flex items-center gap-1">
					<div class="w-2 h-2 bg-black rounded-full"></div>
					<span class="text-muted">OTHERS</span>
				</div>
			</div>
		</div>
	</div>
</section>

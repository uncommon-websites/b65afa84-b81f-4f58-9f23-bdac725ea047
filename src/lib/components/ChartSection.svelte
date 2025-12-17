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
				DETECTION RATE (%)
			</div>

			<!-- X Axis Label -->
			<div class="absolute bottom-2 left-1/2 -translate-x-1/2 text-muted">
				PRICE PER MILLION REQUESTS
			</div>

			<!-- Top Left Legend -->
			<div class="absolute top-4 left-4 flex gap-4 text-[10px] text-muted">
				<span class="bg-gray-200 px-1 rounded text-foreground">Publisher Benchmark</span>
				<span>AI Scraper Detection</span>
				<span>Stealth Bot Detection</span>
			</div>

			<!-- Data Points -->
			
			<!-- Centinel (The Winner) -->
			<div class="absolute top-[12%] left-[18%] flex flex-col items-center group cursor-pointer z-10">
				<div class="flex items-center gap-2 mb-1">
					<span class="text-accent font-bold">CENTINEL</span>
				</div>
				<div class="w-3 h-3 bg-accent rounded-full border-2 border-accent/20"></div>
				<div class="mt-1 text-[10px] text-accent">94% / $3.50</div>
			</div>

			<!-- DataDome -->
			<div class="absolute top-[28%] left-[52%] flex flex-col items-center group cursor-pointer">
				<div class="flex items-center gap-2 mb-1 opacity-0 group-hover:opacity-100 transition-opacity">
					<span class="font-bold">DATADOME</span>
				</div>
				<div class="w-2 h-2 bg-black rounded-full"></div>
				<div class="mt-1 text-[10px] text-muted">72% / $12</div>
			</div>

			<!-- PerimeterX -->
			<div class="absolute top-[35%] left-[58%] flex flex-col items-center group cursor-pointer">
				<div class="flex items-center gap-2 mb-1 opacity-100">
					<span class="font-bold text-[10px]">PERIMETERX</span>
				</div>
				<div class="w-2 h-2 bg-black rounded-full"></div>
				<div class="mt-1 text-[10px] text-muted">68% / $15</div>
			</div>

			<!-- Cloudflare Bot Management -->
			<div class="absolute top-[45%] left-[42%] flex flex-col items-center group cursor-pointer">
				<div class="flex items-center gap-2 mb-1 opacity-100">
					<span class="font-bold text-[10px]">CLOUDFLARE</span>
				</div>
				<div class="w-2 h-2 bg-black rounded-full"></div>
				<div class="mt-1 text-[10px] text-muted">65% / $8</div>
			</div>

			<!-- Generic WAF -->
			<div class="absolute top-[75%] left-[25%] flex flex-col items-center group cursor-pointer">
				<div class="flex items-center gap-2 mb-1 opacity-100">
					<span class="font-bold text-[10px]">GENERIC WAF</span>
				</div>
				<div class="w-2 h-2 bg-black rounded-full"></div>
				<div class="mt-1 text-[10px] text-muted">42% / $2</div>
			</div>

			<!-- Bottom Right Legend -->
			<div class="absolute bottom-4 right-4 flex items-center gap-4 text-[10px]">
				<div class="flex items-center gap-1">
					<div class="w-2 h-2 bg-accent rounded-full"></div>
					<span class="text-accent font-bold">CENTINEL</span>
				</div>
				<div class="flex items-center gap-1">
					<div class="w-2 h-2 bg-black rounded-full"></div>
					<span class="text-muted">COMPETITORS</span>
				</div>
			</div>
		</div>
	</div>
</section>

<section class="pt-20 pb-12 overflow-hidden">
	<div class="container-custom">
		<div class="max-w-4xl mb-12">
			<h1 class="text-4xl md:text-5xl lg:text-6xl font-medium tracking-tight mb-4">
				Stop AI scrapers from stealing your content
			</h1>
			<p class="text-2xl md:text-3xl text-muted font-light">
				Advanced bot protection built by <span class="text-accent">former scraper experts</span>
			</p>
		</div>

		<div class="relative w-full aspect-[2/1] bg-gray-950 rounded-sm overflow-hidden group">
			<!-- Dark Background -->
			<div class="absolute inset-0 bg-gradient-to-br from-gray-900 via-gray-950 to-black"></div>
			
			<!-- Grid Overlay - Network -->
			<div class="absolute inset-0" style="background-image: linear-gradient(rgba(255,255,255,0.03) 1px, transparent 1px), linear-gradient(90deg, rgba(255,255,255,0.03) 1px, transparent 1px); background-size: 60px 60px;"></div>
			
			<!-- Scanning Lines Effect -->
			<div class="absolute inset-0 opacity-20">
				<div class="absolute top-0 left-0 right-0 h-px bg-gradient-to-r from-transparent via-primary-400 to-transparent animate-pulse"></div>
				<div class="absolute top-1/3 left-0 right-0 h-px bg-gradient-to-r from-transparent via-primary-500 to-transparent animate-pulse" style="animation-delay: 0.5s;"></div>
				<div class="absolute top-2/3 left-0 right-0 h-px bg-gradient-to-r from-transparent via-primary-400 to-transparent animate-pulse" style="animation-delay: 1s;"></div>
			</div>
			
			<!-- Bot Detection Visualization -->
			<div class="absolute inset-0 flex items-center justify-center">
				<div class="relative w-full h-full max-w-3xl">
					<!-- Central Detection Core -->
					<div class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2">
						<div class="w-24 h-24 rounded-full border-2 border-primary-500/50 flex items-center justify-center">
							<div class="w-16 h-16 rounded-full bg-primary-500/20 border border-primary-400/60 animate-pulse"></div>
						</div>
						<!-- Radar sweep effect -->
						<div class="absolute inset-0 rounded-full border-2 border-primary-400/30 animate-ping" style="animation-duration: 3s;"></div>
					</div>

					<!-- Incoming Bot Traffic (Red - Left Side) -->
					<div class="absolute top-1/4 left-8 w-3 h-3 bg-red-500 rounded-full animate-pulse"></div>
					<div class="absolute top-1/3 left-16 w-2 h-2 bg-red-400 rounded-full animate-pulse" style="animation-delay: 0.3s;"></div>
					<div class="absolute top-1/2 left-12 w-3 h-3 bg-red-500 rounded-full animate-pulse" style="animation-delay: 0.6s;"></div>
					<div class="absolute top-2/3 left-20 w-2 h-2 bg-red-400 rounded-full animate-pulse" style="animation-delay: 0.9s;"></div>
					<div class="absolute top-3/4 left-10 w-3 h-3 bg-red-500 rounded-full animate-pulse" style="animation-delay: 1.2s;"></div>
					
					<!-- Connection lines from bots to center (being analyzed) -->
					<svg class="absolute inset-0 w-full h-full pointer-events-none opacity-30">
						<line x1="10%" y1="25%" x2="50%" y2="50%" stroke="#ef4444" stroke-width="1" stroke-dasharray="4,4" class="animate-pulse"/>
						<line x1="15%" y1="33%" x2="50%" y2="50%" stroke="#ef4444" stroke-width="1" stroke-dasharray="4,4" class="animate-pulse" style="animation-delay: 0.3s;"/>
						<line x1="12%" y1="50%" x2="50%" y2="50%" stroke="#ef4444" stroke-width="1" stroke-dasharray="4,4" class="animate-pulse" style="animation-delay: 0.6s;"/>
						<line x1="18%" y1="66%" x2="50%" y2="50%" stroke="#ef4444" stroke-width="1" stroke-dasharray="4,4" class="animate-pulse" style="animation-delay: 0.9s;"/>
						<line x1="10%" y1="75%" x2="50%" y2="50%" stroke="#ef4444" stroke-width="1" stroke-dasharray="4,4" class="animate-pulse" style="animation-delay: 1.2s;"/>
					</svg>

					<!-- Legitimate Traffic (Green - Right Side, fewer) -->
					<div class="absolute top-1/3 right-16 w-2 h-2 bg-green-400 rounded-full"></div>
					<div class="absolute top-1/2 right-20 w-2 h-2 bg-green-400 rounded-full" style="animation-delay: 0.5s;"></div>
					<div class="absolute top-2/3 right-12 w-2 h-2 bg-green-400 rounded-full" style="animation-delay: 1s;"></div>
					
					<!-- Connection lines for legitimate traffic -->
					<svg class="absolute inset-0 w-full h-full pointer-events-none opacity-50">
						<line x1="50%" y1="50%" x2="85%" y2="33%" stroke="#22c55e" stroke-width="1.5"/>
						<line x1="50%" y1="50%" x2="82%" y2="50%" stroke="#22c55e" stroke-width="1.5"/>
						<line x1="50%" y1="50%" x2="88%" y2="66%" stroke="#22c55e" stroke-width="1.5"/>
					</svg>

					<!-- Detection Labels -->
					<div class="absolute top-1/4 left-1/2 -translate-x-1/2 -translate-y-12 text-xs font-mono text-primary-400 opacity-60">
						Behavioral Analysis
					</div>
					<div class="absolute bottom-1/4 left-1/2 -translate-x-1/2 translate-y-12 text-xs font-mono text-primary-400 opacity-60">
						Network Fingerprinting
					</div>
				</div>
			</div>

			<!-- Floating Metrics -->
			<div class="absolute top-8 left-8 bg-black/60 backdrop-blur-sm px-3 py-2 rounded border border-primary-500/30 text-xs font-mono text-primary-400">
				<div class="flex items-center gap-2">
					<span class="w-2 h-2 bg-red-500 rounded-full animate-pulse"></span>
					<span class="text-white">Bot Detected</span>
				</div>
			</div>
			
			<div class="absolute bottom-8 right-8 bg-black/60 backdrop-blur-sm px-3 py-2 rounded border border-green-500/30 text-xs font-mono text-green-400">
				<div class="flex items-center gap-2">
					<span class="w-2 h-2 bg-green-500 rounded-full"></span>
					<span class="text-white">24% Traffic Blocked</span>
				</div>
			</div>

			<div class="absolute top-1/2 right-12 bg-black/60 backdrop-blur-sm px-3 py-2 rounded border border-primary-500/30 text-xs font-mono text-white">
				500M+ Requests/Month
			</div>
		</div>
	</div>
</section>

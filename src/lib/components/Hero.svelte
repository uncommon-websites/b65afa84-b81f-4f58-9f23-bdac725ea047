<script lang="ts">
	import { onMount } from 'svelte';

	interface RequestItem {
		id: number;
		ip: string;
		path: string;
		agent: string;
		status: 'blocked' | 'allowed';
		delay: number;
	}

	let requests: RequestItem[] = $state([]);
	let counter = $state(0);
	let blockedCount = $state(0);
	let allowedCount = $state(0);

	const paths = ['/api/v2/products', '/search?q=*', '/sitemap.xml', '/robots.txt', '/api/users', '/checkout', '/catalog/export', '/.env', '/wp-admin', '/graphql'];
	const agents = ['GPTBot/1.0', 'Mozilla/5.0', 'Scrapy/2.11', 'curl/8.4.0', 'Python-urllib/3.11', 'Chrome/120', 'Bytespider', 'CCBot/2.0', 'ClaudeBot', 'Safari/17.2'];
	const ips = ['45.33.', '192.168.', '10.0.', '172.16.', '203.0.', '198.51.', '91.108.', '185.220.', '23.129.', '104.21.'];

	function generateRequest(): RequestItem {
		const isBot = Math.random() > 0.35;
		return {
			id: counter++,
			ip: ips[Math.floor(Math.random() * ips.length)] + Math.floor(Math.random() * 255) + '.' + Math.floor(Math.random() * 255),
			path: paths[Math.floor(Math.random() * paths.length)],
			agent: agents[Math.floor(Math.random() * agents.length)],
			status: isBot ? 'blocked' : 'allowed',
			delay: Math.random() * 0.3
		};
	}

	onMount(() => {
		// Initial batch
		const initialRequests: RequestItem[] = [];
		for (let i = 0; i < 6; i++) {
			const req = generateRequest();
			req.delay = i * 0.15;
			initialRequests.push(req);
			if (req.status === 'blocked') blockedCount++;
			else allowedCount++;
		}
		requests = initialRequests;

		const interval = setInterval(() => {
			const newReq = generateRequest();
			if (newReq.status === 'blocked') blockedCount++;
			else allowedCount++;

			requests = [...requests.slice(-7), newReq];
		}, 1800);

		return () => clearInterval(interval);
	});
</script>

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

		<div class="relative w-full aspect-[4/3] md:aspect-[2/1] bg-zinc-950 rounded-sm overflow-hidden">
			<!-- Subtle gradient background -->
			<div class="absolute inset-0 bg-[radial-gradient(ellipse_at_top,_var(--tw-gradient-stops))] from-zinc-900 via-zinc-950 to-black"></div>

			<!-- Main content grid -->
			<div class="absolute inset-0 flex flex-col md:flex-row">

				<!-- Top/Left panel: Request stream -->
				<div class="flex-1 flex flex-col justify-center px-4 py-4 md:pl-10 md:pr-4 relative">
					<!-- Divider line -->
					<div class="hidden md:block absolute right-0 top-[15%] bottom-[15%] w-px bg-gradient-to-b from-transparent via-zinc-700 to-transparent"></div>
					<div class="md:hidden absolute bottom-0 left-[15%] right-[15%] h-px bg-gradient-to-r from-transparent via-zinc-700 to-transparent"></div>

					<div class="space-y-1 md:space-y-1.5 overflow-hidden">
						{#each requests.slice(0, 5) as req (req.id)}
							<div
								class="request-row flex items-center gap-2 md:gap-3 py-1 md:py-1.5 px-2 md:px-3 rounded-sm font-mono text-[9px] md:text-xs transition-all duration-500 {req.status === 'blocked' ? 'bg-red-500/10' : 'bg-blue-500/10'}"
								style="animation-delay: {req.delay}s"
							>
								<span class="w-1.5 h-1.5 rounded-full flex-shrink-0 {req.status === 'blocked' ? 'bg-red-500' : 'bg-blue-400'}"></span>
								<span class="text-zinc-500 truncate">{req.ip}</span>
								<span
									class="ml-auto uppercase text-[8px] md:text-[10px] tracking-wider font-medium px-1.5 py-0.5 rounded-sm {req.status === 'blocked' ? 'text-red-400 bg-red-500/20' : 'text-blue-400 bg-blue-500/20'}"
								>
									{req.status}
								</span>
							</div>
						{/each}
					</div>
				</div>

				<!-- Bottom/Right panel: Stats -->
				<div class="flex-1 flex items-center justify-center relative px-4 py-4">
					<!-- Stats grid for mobile -->
					<div class="flex items-center gap-6 md:gap-0 md:block">
						<!-- Central shield/filter graphic - hidden on mobile -->
						<div class="hidden md:block relative">
							<div class="w-44 h-44 rounded-full border border-zinc-800 flex items-center justify-center relative">
								<div class="absolute inset-0 rounded-full overflow-hidden">
									<div class="scanner-arc absolute inset-0 rounded-full" style="background: conic-gradient(from 0deg, transparent 0deg, rgba(59, 130, 246, 0.2) 60deg, transparent 120deg);"></div>
								</div>
								<div class="w-28 h-28 rounded-full border border-zinc-700/50 flex items-center justify-center">
									<div class="w-14 h-14 rounded-full bg-gradient-to-br from-blue-500/20 to-blue-600/10 border border-blue-500/30 flex items-center justify-center">
										<div class="w-4 h-4 rounded-full bg-blue-400/60 core-pulse"></div>
									</div>
								</div>
							</div>
						</div>

						<!-- Mobile stats display -->
						<div class="flex md:hidden items-center gap-8">
							<div class="text-center">
								<div class="font-mono text-[9px] text-blue-400/80 mb-0.5">ALLOWED</div>
								<div class="font-mono text-2xl text-blue-400 tabular-nums">{allowedCount}</div>
							</div>
							<div class="text-center">
								<div class="font-mono text-[9px] text-red-400/80 mb-0.5">BLOCKED</div>
								<div class="font-mono text-2xl text-red-400 tabular-nums">{blockedCount}</div>
							</div>
							<div class="text-center">
								<div class="font-mono text-[9px] text-zinc-500 mb-0.5">TOTAL</div>
								<div class="font-mono text-2xl text-zinc-300 tabular-nums">{blockedCount + allowedCount}</div>
							</div>
						</div>
					</div>

					<!-- Desktop stats overlay -->
					<div class="hidden md:block absolute bottom-8 right-8 text-right">
						<div class="font-mono text-[10px] text-zinc-500 mb-1">REQUESTS ANALYZED</div>
						<div class="font-mono text-3xl text-zinc-300 tabular-nums tracking-tight">
							{(blockedCount + allowedCount).toLocaleString()}
						</div>
					</div>

					<div class="hidden md:block absolute top-8 right-8 text-right">
						<div class="font-mono text-[10px] text-red-400/80 mb-0.5">BLOCKED</div>
						<div class="font-mono text-xl text-red-400 tabular-nums">{blockedCount}</div>
					</div>

					<div class="hidden md:block absolute top-8 left-8">
						<div class="font-mono text-[10px] text-blue-400/80 mb-0.5">ALLOWED</div>
						<div class="font-mono text-xl text-blue-400 tabular-nums">{allowedCount}</div>
					</div>
				</div>
			</div>

			<!-- Bottom status bar -->
			<div class="absolute bottom-0 left-0 right-0 h-7 md:h-8 bg-zinc-900/80 border-t border-zinc-800/50 flex items-center px-3 md:px-6 gap-4 md:gap-6 font-mono text-[9px] md:text-[10px]">
				<div class="flex items-center gap-1.5 md:gap-2">
					<span class="w-1.5 h-1.5 rounded-full bg-blue-400 status-blink"></span>
					<span class="text-zinc-400">ACTIVE</span>
				</div>
				<div class="text-zinc-600">|</div>
				<div class="text-zinc-500"><span class="text-zinc-400">2.3ms</span></div>
				<div class="ml-auto text-zinc-600">v2.4.1</div>
			</div>
		</div>
	</div>
</section>

<style>
	.request-row {
		animation: slideIn 0.5s ease-out forwards;
		opacity: 0;
		transform: translateX(-20px);
	}

	@keyframes slideIn {
		to {
			opacity: 1;
			transform: translateX(0);
		}
	}

	.scanner-arc {
		animation: scan 4s linear infinite;
	}

	@keyframes scan {
		from { transform: rotate(0deg); }
		to { transform: rotate(360deg); }
	}

	.core-pulse {
		animation: corePulse 2s ease-in-out infinite;
	}

	@keyframes corePulse {
		0%, 100% { opacity: 0.6; transform: scale(1); }
		50% { opacity: 1; transform: scale(1.1); }
	}

	.particle-float {
		animation: particleIn 3s ease-in-out infinite;
	}

	@keyframes particleIn {
		0%, 100% { opacity: 0; transform: translate(0, 0) scale(0.5); }
		20% { opacity: 0.8; transform: translate(10px, 5px) scale(1); }
		40% { opacity: 0.4; transform: translate(20px, 10px) scale(0.8); }
		60% { opacity: 0; transform: translate(30px, 15px) scale(0.3); }
	}

	.particle-float-out {
		animation: particleOut 3.5s ease-in-out infinite;
	}

	@keyframes particleOut {
		0%, 100% { opacity: 0; transform: translate(0, 0) scale(0.5); }
		30% { opacity: 0.7; transform: translate(-15px, -8px) scale(1); }
		60% { opacity: 0.9; transform: translate(-30px, -15px) scale(0.9); }
		100% { opacity: 0; transform: translate(-50px, -25px) scale(0.5); }
	}

	.status-blink {
		animation: blink 2s ease-in-out infinite;
	}

	@keyframes blink {
		0%, 100% { opacity: 1; }
		50% { opacity: 0.4; }
	}
</style>

<script lang="ts">
	import FeatureBlock from './FeatureBlock.svelte';
</script>

<!-- Block 1: Network-level bot detection -->
<FeatureBlock
	title="Network-level bot detection"
	description="Detect stealth bots that evade traditional fingerprinting. Built from 15+ years of scraper expertise."
	buttons={[
		{ text: "SEE HOW IT WORKS", icon: true },
		{ text: "REQUEST DEMO" }
	]}
>
	<div class="w-full h-full bg-white border border-border rounded overflow-hidden font-mono text-[10px]">
		<!-- Header -->
		<div class="flex items-center justify-between p-2 border-b border-border bg-gray-50">
			<div class="flex items-center gap-2 text-muted">
				<div class="w-4 h-4 rounded-full border-2 border-accent flex items-center justify-center">
					<div class="w-1.5 h-1.5 bg-accent rounded-full"></div>
				</div>
				Network Analysis
			</div>
			<div class="flex items-center gap-1">
				<span class="w-2 h-2 bg-green-500 rounded-full"></span>
				<span class="text-green-600">LIVE</span>
			</div>
		</div>

		<!-- Detection log -->
		<div class="divide-y divide-border/50">
			{#each [
				{ ip: '185.220.101.42', type: 'GPTBot', level: 'high', status: 'blocked' },
				{ ip: '91.108.56.178', type: 'Scrapy', level: 'high', status: 'blocked' },
				{ ip: '66.249.66.1', type: 'Googlebot', level: 'safe', status: 'allowed' },
				{ ip: '45.33.32.156', type: 'ClaudeBot', level: 'high', status: 'blocked' },
				{ ip: '157.55.39.1', type: 'Bingbot', level: 'safe', status: 'allowed' }
			] as entry}
				<div class="flex items-center gap-3 p-2">
					<span class="w-1.5 h-1.5 rounded-full {entry.status === 'blocked' ? 'bg-red-500' : 'bg-blue-500'}"></span>
					<span class="text-muted w-28">{entry.ip}</span>
					<span class="text-foreground flex-1">{entry.type}</span>
					<span class="px-1.5 py-0.5 rounded text-[9px] uppercase {entry.status === 'blocked' ? 'bg-red-100 text-red-600' : 'bg-blue-100 text-blue-600'}">
						{entry.status}
					</span>
				</div>
			{/each}
		</div>

		<!-- Footer stats -->
		<div class="flex items-center justify-between p-2 border-t border-border bg-gray-50 text-muted">
			<div class="flex items-center gap-4">
				<div class="flex items-center gap-1">
					<span class="w-2 h-2 bg-red-500 rounded-full"></span>
					<span>3 blocked</span>
				</div>
				<div class="flex items-center gap-1">
					<span class="w-2 h-2 bg-blue-500 rounded-full"></span>
					<span>2 allowed</span>
				</div>
			</div>
			<div class="text-foreground font-medium">+30% detection</div>
		</div>
	</div>
</FeatureBlock>

<!-- Block 2: Real-time behavioral fingerprinting -->
<FeatureBlock 
	title="Real-time behavioral fingerprinting" 
	description="Advanced fingerprinting analyzes behavior patterns to identify sophisticated bots in milliseconds"
	buttons={[
		{ text: "VIEW TECHNOLOGY", icon: true }
	]}
	alignRight={true}
>
	<div class="w-full max-w-md bg-white border border-border rounded p-6 flex flex-col gap-4">
		<div class="flex items-center gap-2 text-xs font-mono text-muted">
			<div class="w-4 h-4 border border-current rounded-sm flex items-center justify-center">
				<div class="w-2 h-2 bg-current rounded-[1px]"></div>
			</div>
			Analyzing request fingerprint...
		</div>
		<div class="w-full bg-gray-100 h-1.5 rounded-full overflow-hidden">
			<div class="bg-accent h-full w-5/6"></div>
		</div>
		<div class="flex gap-1">
			{#each Array(20) as _, idx}
				<div class="w-1 h-3 {idx < 15 ? 'bg-red-400' : 'bg-gray-200'}"></div>
			{/each}
		</div>
		<div class="mt-2 flex items-center gap-2 text-[10px] text-red-600 font-mono uppercase">
			<span class="w-3 h-3 border border-current rounded-full flex items-center justify-center">!</span>
			BOT SIGNATURE MATCHED
		</div>
	</div>
</FeatureBlock>

<!-- Block 3: Publisher dashboard & analytics -->
<FeatureBlock 
	title="Publisher dashboard & analytics" 
	description="Real-time visibility into bot traffic, cost savings, and protection effectiveness across all your sites"
	buttons={[
		{ text: "EXPLORE DASHBOARD", icon: true }
	]}
>
	<div class="w-full h-full bg-white border border-border rounded overflow-hidden font-mono text-[10px]">
		<div class="grid grid-cols-4 gap-2 p-2 border-b border-border bg-gray-50 text-muted">
			<div>TIMESTAMP</div>
			<div>SOURCE IP</div>
			<div>STATUS</div>
			<div>THREAT LEVEL</div>
		</div>
		{#each [1, 2, 3, 4, 5, 6] as i}
			<div class="grid grid-cols-4 gap-2 p-2 border-b border-border/50 items-center">
				<div class="text-muted">{String(i).padStart(2, '0')}:3{i}:12</div>
				<div class="flex items-center gap-2">
					<div class="w-3 h-3 rounded-full {i % 3 === 0 ? 'bg-red-400/20' : 'bg-green-400/20'}"></div>
					<span class="{i % 3 === 0 ? 'text-red-600' : 'text-green-600'}">185.{i}.{i * 2}.{i * 3}</span>
				</div>
				<div class="text-xs {i % 3 === 0 ? 'text-red-600' : 'text-green-600'}">{i % 3 === 0 ? 'BLOCKED' : 'ALLOWED'}</div>
				<div class="flex gap-0.5">
					{#each Array(5) as _, idx}
						<div class="w-1 h-3 {idx < (i % 3 === 0 ? 4 : 1) ? 'bg-red-400' : 'bg-gray-200'}"></div>
					{/each}
				</div>
			</div>
		{/each}
	</div>
</FeatureBlock>

<!-- Block 4: Intelligent crawler management -->
<FeatureBlock 
	title="Intelligent crawler management" 
	description="Whitelist trusted crawlers like Google and Bing for SEO, block harmful bots. Zero false positives."
	buttons={[
		{ text: "MANAGE CRAWLERS", icon: true }
	]}
	alignRight={true}
>
	<div class="w-full h-full bg-white border border-border rounded overflow-hidden font-mono text-[10px]">
		<div class="grid grid-cols-4 gap-2 p-2 border-b border-border bg-gray-50 text-muted">
			<div>CRAWLER</div>
			<div>TYPE</div>
			<div>STATUS</div>
			<div>ACTION</div>
		</div>
		{#each [
			{ name: 'Googlebot', type: 'Search Engine', allowed: true },
			{ name: 'Bingbot', type: 'Search Engine', allowed: true },
			{ name: 'GPTBot', type: 'AI Scraper', allowed: false },
			{ name: 'ClaudeBot', type: 'AI Scraper', allowed: false },
			{ name: 'Unknown Bot', type: 'Suspicious', allowed: false },
			{ name: 'Facebook', type: 'Social Media', allowed: true }
		] as crawler}
			<div class="grid grid-cols-4 gap-2 p-2 border-b border-border/50 items-center">
				<div class="text-foreground">{crawler.name}</div>
				<div class="text-muted">{crawler.type}</div>
				<div class="flex items-center gap-1">
					<div class="w-2 h-2 rounded-full {crawler.allowed ? 'bg-green-500' : 'bg-red-500'}"></div>
					<span class="{crawler.allowed ? 'text-green-600' : 'text-red-600'}">{crawler.allowed ? 'ALLOW' : 'BLOCK'}</span>
				</div>
				<div class="text-xs text-muted">{crawler.allowed ? '✓' : '✕'}</div>
			</div>
		{/each}
	</div>
</FeatureBlock>

<!-- Block 5: Seamless CMS/CDN integration -->
<FeatureBlock 
	title="Seamless CMS and CDN integration" 
	description="Deploy in hours with plugins for WordPress, Drupal, Magento, or integrate with Cloudflare, Akamai, Fastly"
	buttons={[
		{ text: "VIEW INTEGRATIONS", icon: true }
	]}
>
	<div class="w-full h-full bg-white border border-border rounded p-4 flex flex-col gap-4">
		<div class="flex items-center justify-between border-b border-border pb-2">
			<div class="text-[10px] font-mono text-muted flex items-center gap-2">
				<span class="w-2 h-2 bg-green-500 rounded-full"></span>
				Integration status
			</div>
		</div>
		
		<!-- Integration Grid -->
		<div class="grid grid-cols-3 gap-2">
			{#each [
				{ name: 'WordPress', status: 'active' },
				{ name: 'Drupal', status: 'active' },
				{ name: 'Magento', status: 'active' },
				{ name: 'Cloudflare', status: 'active' },
				{ name: 'Akamai', status: 'active' },
				{ name: 'Fastly', status: 'active' }
			] as integration}
				<div class="border border-border rounded p-2 flex flex-col items-center justify-center gap-1">
					<div class="w-6 h-6 bg-gray-100 rounded flex items-center justify-center text-[8px] font-bold">
						{integration.name.slice(0, 2).toUpperCase()}
					</div>
					<div class="text-[8px] font-mono text-center">{integration.name}</div>
					<div class="w-1.5 h-1.5 bg-green-500 rounded-full"></div>
				</div>
			{/each}
		</div>

		<div class="mt-auto space-y-2">
			<div class="flex items-center gap-2 text-[10px] text-green-600 font-mono">
				<span class="w-3 h-3 border border-current rounded-full flex items-center justify-center text-[8px]">✓</span>
				All integrations operational
			</div>
			<div class="bg-gray-50 p-2 rounded border border-border flex gap-2 items-center justify-between">
				<div class="text-[10px] text-muted">Setup time</div>
				<div class="text-[10px] font-bold">Hours, not days</div>
			</div>
		</div>
	</div>
</FeatureBlock>

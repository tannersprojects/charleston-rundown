<script lang="ts">
	import { Button } from '$lib/components/ui/button';
	import { Card, CardContent } from '$lib/components/ui/card';
	import { Badge } from '$lib/components/ui/badge';
	import { Search, Calendar, Clock } from '@lucide/svelte';
	import rainbowRow from '$lib/assets/charleston-images/Charleston Rainbow Row.jpg';
	import historicDistrict from '$lib/assets/charleston-images/historic-district.jpg';
	import mtPleasant from '$lib/assets/charleston-images/mt-pleasant-ion.png';

	// Blog posts data
	const blogPosts = [
		{
			id: 1,
			title: "First-Time Homebuyer's Guide to Charleston",
			slug: 'first-time-buyers-guide',
			excerpt:
				'Everything you need to know about buying your first home in Charleston, from neighborhood selection to financing options and local programs.',
			date: 'October 15, 2025',
			readTime: '5 min read',
			category: 'Buying Guide',
			featured: true,
			image: historicDistrict
		},
		{
			id: 2,
			title: "Mount Pleasant vs West Ashley: A Local's Perspective",
			slug: 'mount-pleasant-vs-west-ashley',
			excerpt:
				"Comparing Charleston's most popular neighborhoods to help you decide where to call home based on lifestyle, amenities, and value.",
			date: 'October 10, 2025',
			readTime: '7 min read',
			category: 'Neighborhood Guide',
			featured: true,
			image: mtPleasant
		},
		{
			id: 3,
			title: 'October 2025 Charleston Market Update',
			slug: 'october-2025-market-update',
			excerpt:
				'Current market trends, pricing insights, and what buyers and sellers can expect in the Charleston real estate market this fall.',
			date: 'October 5, 2025',
			readTime: '4 min read',
			category: 'Market Update',
			featured: true,
			image: rainbowRow
		}
	];

	const categories = ['All', 'Buying Guide', 'Neighborhood Guide', 'Market Update'];
	let selectedCategory = 'All';
	let searchTerm = '';

	$: filteredPosts = blogPosts.filter((post) => {
		const matchesCategory = selectedCategory === 'All' || post.category === selectedCategory;
		const matchesSearch =
			searchTerm === '' ||
			post.title.toLowerCase().includes(searchTerm.toLowerCase()) ||
			post.excerpt.toLowerCase().includes(searchTerm.toLowerCase());
		return matchesCategory && matchesSearch;
	});

	// Function to get alt text for images
	function getImageAlt(title: string): string {
		if (title.includes('Mount Pleasant') || title.includes('West Ashley')) {
			return 'Mount Pleasant, Charleston';
		} else if (title.includes('Historic') || title.includes('First-Time')) {
			return 'Historic Downtown Charleston';
		} else if (title.includes('Market')) {
			return 'Rainbow Row, Charleston';
		}
		return 'Charleston Real Estate';
	}
</script>

<svelte:head>
	<title>Charleston Real Estate Blog - Kai Fischer</title>
	<meta
		name="description"
		content="Expert insights on Charleston real estate market, neighborhood guides, and home buying tips from local real estate agent Kai Fischer."
	/>
</svelte:head>

<div class="page-container">
	<div class="page-content-extra-wide">
		<div class="space-y-12">
			<!-- Hero Section -->
			<div class="space-y-6 text-center">
				<h1 class="text-foreground text-4xl font-bold tracking-tight md:text-5xl">
					Charleston Real Estate Blog
				</h1>
				<p class="text-muted-foreground mx-auto max-w-3xl text-xl">
					Stay informed with expert insights on the Charleston real estate market, neighborhood
					guides, home buying tips, and local market trends.
				</p>
			</div>

			<!-- Search and Filter -->
			<Card class="border-primary/20 bg-background/50 backdrop-blur-sm">
				<CardContent class="p-6">
					<div class="flex flex-col gap-4 md:flex-row md:items-center md:justify-between">
						<!-- Search Bar -->
						<div class="relative flex-1">
							<Search
								class="text-muted-foreground absolute left-3 top-1/2 h-5 w-5 -translate-y-1/2 transform"
							/>
							<input
								type="text"
								bind:value={searchTerm}
								placeholder="Search articles..."
								class="border-border bg-background text-foreground placeholder:text-muted-foreground focus:border-primary focus:ring-primary/20 w-full rounded-md border py-3 pl-10 pr-4 focus:outline-none focus:ring-2"
							/>
						</div>

						<!-- Category Filter -->
						<div class="flex flex-wrap gap-2">
							{#each categories as category}
								<Button
									variant={selectedCategory === category ? 'default' : 'outline'}
									size="sm"
									onclick={() => (selectedCategory = category)}
									class={selectedCategory === category
										? ''
										: 'border-primary/20 hover:border-primary/40'}
								>
									{category}
								</Button>
							{/each}
						</div>
					</div>
				</CardContent>
			</Card>

			<!-- Featured Posts -->
			{#if selectedCategory === 'All' && searchTerm === ''}
				<div>
					<h2 class="text-foreground mb-6 text-2xl font-semibold">Featured Articles</h2>
					<div class="grid grid-cols-1 gap-8 md:grid-cols-3">
						{#each blogPosts.filter((post) => post.featured) as post}
							<Card class="border-primary/20 transition-all hover:scale-105 hover:shadow-lg">
								<CardContent class="p-0">
									<!-- Featured Image -->
									<div class="h-48 overflow-hidden">
										<img
											src={post.image}
											alt={getImageAlt(post.title)}
											class="h-full w-full object-cover transition-transform duration-300 hover:scale-105"
										/>
									</div>
									<div class="p-6">
										<div class="text-muted-foreground mb-3 flex items-center space-x-4 text-sm">
											<div class="flex items-center space-x-1">
												<Calendar class="h-4 w-4" />
												<span>{post.date}</span>
											</div>
											<div class="flex items-center space-x-1">
												<Clock class="h-4 w-4" />
												<span>{post.readTime}</span>
											</div>
										</div>
										<div class="mb-2">
											<Badge variant="secondary">{post.category}</Badge>
										</div>
										<h3 class="text-foreground mb-3 line-clamp-2 text-xl font-semibold">
											{post.title}
										</h3>
										<p class="text-muted-foreground mb-4 line-clamp-3">
											{post.excerpt}
										</p>
										<Button
											href="/blog/{post.slug}"
											variant="ghost"
											class="text-primary hover:text-primary/80 h-auto p-0"
										>
											Read More →
										</Button>
									</div>
								</CardContent>
							</Card>
						{/each}
					</div>
				</div>
			{/if}

			<!-- All Posts -->
			<div>
				<h2 class="text-foreground mb-6 text-2xl font-semibold">
					{selectedCategory === 'All' && searchTerm === ''
						? 'All Articles'
						: `Articles ${selectedCategory !== 'All' ? `in ${selectedCategory}` : ''}${searchTerm ? ` matching "${searchTerm}"` : ''}`}
				</h2>

				{#if filteredPosts.length > 0}
					<div class="grid grid-cols-1 gap-8 md:grid-cols-2 lg:grid-cols-3">
						{#each filteredPosts as post}
							<Card class="border-primary/20 transition-all hover:scale-105 hover:shadow-lg">
								<CardContent class="p-0">
									<!-- Featured Image -->
									<div class="h-48 overflow-hidden">
										<img
											src={post.image}
											alt={getImageAlt(post.title)}
											class="h-full w-full object-cover transition-transform duration-300 hover:scale-105"
										/>
									</div>
									<div class="p-6">
										<div class="text-muted-foreground mb-3 flex items-center space-x-4 text-sm">
											<div class="flex items-center space-x-1">
												<Calendar class="h-4 w-4" />
												<span>{post.date}</span>
											</div>
											<div class="flex items-center space-x-1">
												<Clock class="h-4 w-4" />
												<span>{post.readTime}</span>
											</div>
										</div>
										<div class="mb-2">
											<Badge variant="secondary">{post.category}</Badge>
										</div>
										<h3 class="text-foreground mb-3 line-clamp-2 text-xl font-semibold">
											{post.title}
										</h3>
										<p class="text-muted-foreground mb-4 line-clamp-3">
											{post.excerpt}
										</p>
										<Button
											href="/blog/{post.slug}"
											variant="ghost"
											class="text-primary hover:text-primary/80 h-auto p-0"
										>
											Read More →
										</Button>
									</div>
								</CardContent>
							</Card>
						{/each}
					</div>
				{:else}
					<div class="py-12 text-center">
						<div
							class="bg-primary/10 mx-auto mb-4 flex h-24 w-24 items-center justify-center rounded-full"
						>
							<Search class="text-primary h-12 w-12" />
						</div>
						<h3 class="text-foreground mb-2 text-xl font-semibold">No articles found</h3>
						<p class="text-muted-foreground">Try adjusting your search terms or category filter.</p>
					</div>
				{/if}
			</div>

			<!-- Newsletter Signup -->
			<div class="text-center">
				<Card class="border-primary/20 from-primary/5 to-primary/10 bg-gradient-to-br">
					<CardContent class="p-8">
						<h2 class="text-foreground mb-4 text-2xl font-bold">Stay Updated</h2>
						<p class="text-muted-foreground mx-auto mb-6 max-w-2xl">
							Get the latest Charleston real estate insights, market updates, and neighborhood
							guides delivered to your inbox.
						</p>
						<div class="mx-auto flex max-w-md flex-col gap-4 sm:flex-row">
							<input
								type="email"
								placeholder="Enter your email"
								class="border-border bg-background text-foreground placeholder:text-muted-foreground focus:border-primary focus:ring-primary/20 flex-1 rounded-md border px-4 py-3 focus:outline-none focus:ring-2"
							/>
							<Button size="lg" class="px-6 py-3">Subscribe</Button>
						</div>
					</CardContent>
				</Card>
			</div>
		</div>
	</div>
</div>

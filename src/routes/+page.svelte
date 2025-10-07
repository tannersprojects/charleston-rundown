<script lang="ts">
	import { Button } from '$lib/components/ui/button';
	import { Card, CardContent } from '$lib/components/ui/card';
	import headshot from '$lib/assets/headshot.jpeg';
	import heroSkyline from '$lib/assets/charleston-images/hero-charleston-skyline.webp';
	import rainbowRow from '$lib/assets/charleston-images/Charleston Rainbow Row.jpg';
	import historicDistrict from '$lib/assets/charleston-images/historic-district.jpg';
	import mtPleasant from '$lib/assets/charleston-images/mt-pleasant-ion.png';
</script>

<div class="page-container">
	<div class="page-content-extra-wide">
		<div class="space-y-8 text-center">
			<!-- Hero Section with Charleston Background -->
			<div class="relative overflow-hidden rounded-2xl shadow-2xl">
				<!-- Background Image -->
				<div class="absolute inset-0">
					<img
						src={heroSkyline}
						alt="Charleston Skyline"
						class="h-full w-full object-cover"
						loading="eager"
					/>
					<!-- Overlay for text readability -->
					<div class="absolute inset-0 bg-black/40"></div>
				</div>

				<!-- Hero Content -->
				<div class="relative space-y-6 px-8 py-16 text-center text-white md:px-12 md:py-20">
					<h1 class="text-4xl font-bold tracking-tight md:text-6xl">
						Welcome to the
						<span class="text-yellow-300">Holy City</span>
					</h1>
					<p
						class="mx-auto max-w-2xl text-xl text-white [text-shadow:0_4px_24px_rgba(0,0,0,0.85),0_1.5px_0_rgba(0,0,0,0.7)] md:text-2xl"
					>
						Your premier destination for real estate in beautiful Charleston. Find your dream home
						in the Historic District, Mount Pleasant, or anywhere in the Lowcountry.
					</p>
					<div class="flex flex-col justify-center gap-4 sm:flex-row">
						<Button href="/properties" size="lg" class="px-8 py-3 text-lg">View Properties</Button>
						<Button
							href="/contact"
							variant="outline"
							size="lg"
							class="border-black/20 px-8 py-3 text-lg text-black"
						>
							Schedule Consultation
						</Button>
					</div>
				</div>
			</div>

			<!-- Feature Cards -->
			<div class="mt-16 grid grid-cols-1 gap-6 md:grid-cols-3">
				<Card class="border-primary/20 transition-shadow hover:shadow-lg">
					<CardContent class="space-y-3 p-6 text-center">
						<div
							class="bg-primary/10 mx-auto flex h-12 w-12 items-center justify-center rounded-full"
						>
							<svg
								class="text-primary h-6 w-6"
								fill="none"
								stroke="currentColor"
								viewBox="0 0 24 24"
							>
								<path
									stroke-linecap="round"
									stroke-linejoin="round"
									stroke-width="2"
									d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6"
								></path>
							</svg>
						</div>
						<h3 class="text-lg font-semibold">Expert Guidance</h3>
						<p class="text-muted-foreground text-sm">
							Professional real estate expertise to guide you through every step
						</p>
					</CardContent>
				</Card>

				<Card class="border-primary/20 transition-shadow hover:shadow-lg">
					<CardContent class="space-y-3 p-6 text-center">
						<div
							class="bg-primary/10 mx-auto flex h-12 w-12 items-center justify-center rounded-full"
						>
							<svg
								class="text-primary h-6 w-6"
								fill="none"
								stroke="currentColor"
								viewBox="0 0 24 24"
							>
								<path
									stroke-linecap="round"
									stroke-linejoin="round"
									stroke-width="2"
									d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"
								></path>
							</svg>
						</div>
						<h3 class="text-lg font-semibold">Prime Locations</h3>
						<p class="text-muted-foreground text-sm">
							Access to the best properties in Charleston's most desirable neighborhoods
						</p>
					</CardContent>
				</Card>

				<Card class="border-primary/20 transition-shadow hover:shadow-lg">
					<CardContent class="space-y-3 p-6 text-center">
						<div
							class="bg-primary/10 mx-auto flex h-12 w-12 items-center justify-center rounded-full"
						>
							<svg
								class="text-primary h-6 w-6"
								fill="none"
								stroke="currentColor"
								viewBox="0 0 24 24"
							>
								<path
									stroke-linecap="round"
									stroke-linejoin="round"
									stroke-width="2"
									d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"
								></path>
							</svg>
						</div>
						<h3 class="text-lg font-semibold">Trusted Service</h3>
						<p class="text-muted-foreground text-sm">
							Dedicated support throughout your real estate journey
						</p>
					</CardContent>
				</Card>
			</div>

			<!-- About Me Snippet -->
			<div class="mt-20">
				<Card class="border-primary/20 bg-background/50 backdrop-blur-sm">
					<CardContent class="p-8 md:p-12">
						<div
							class="flex flex-col items-center space-y-6 text-center md:flex-row md:space-x-8 md:space-y-0 md:text-left"
						>
							<!-- Professional Headshot -->
							<div class="flex-shrink-0">
								<div class="ring-primary/20 relative overflow-hidden rounded-full shadow-lg ring-4">
									<img
										src={headshot}
										alt="Kai Fischer - Charleston Real Estate Agent"
										class="h-32 w-32 object-cover transition-transform duration-300 hover:scale-105 md:h-40 md:w-40"
										loading="eager"
									/>
								</div>
							</div>

							<!-- About Content -->
							<div class="flex-1 space-y-4">
								<h2 class="text-foreground text-2xl font-bold md:text-3xl">Meet Kai Fischer</h2>
								<p class="text-muted-foreground text-lg">
									Your trusted Charleston real estate expert with deep local knowledge and a passion
									for helping clients find their perfect home in the Lowcountry.
								</p>
								<p class="text-muted-foreground text-base">
									With years of experience in Charleston's diverse neighborhoods, I understand what
									makes each area special and can guide you to the perfect location for your
									lifestyle and budget.
								</p>
								<div class="pt-2">
									<Button
										href="/about"
										variant="outline"
										class="border-primary/20 hover:border-primary/40"
									>
										Learn More About Me
									</Button>
								</div>
							</div>
						</div>
					</CardContent>
				</Card>
			</div>

			<!-- Featured Blog Posts -->
			<div class="mt-20">
				<div class="mb-12 text-center">
					<h2 class="text-foreground text-3xl font-bold md:text-4xl">
						Charleston Real Estate Insights
					</h2>
					<p class="text-muted-foreground mx-auto mt-4 max-w-2xl text-lg">
						Stay informed with expert insights on the Charleston real estate market, neighborhood
						guides, and home buying tips.
					</p>
				</div>

				<div class="grid grid-cols-1 gap-8 md:grid-cols-3">
					<!-- Blog Post 1 -->
					<Card class="border-primary/20 transition-all hover:scale-105 hover:shadow-lg">
						<CardContent class="p-0">
							<!-- Featured Image -->
							<div class="h-48 overflow-hidden">
								<img
									src={historicDistrict}
									alt="Historic Downtown Charleston"
									class="h-full w-full object-cover transition-transform duration-300 hover:scale-105"
								/>
							</div>
							<div class="p-6">
								<div class="text-muted-foreground mb-2 flex items-center space-x-2 text-sm">
									<span>October 15, 2025</span>
									<span>•</span>
									<span>5 min read</span>
								</div>
								<h3 class="text-foreground mb-3 line-clamp-2 text-xl font-semibold">
									First-Time Homebuyer's Guide to Charleston
								</h3>
								<p class="text-muted-foreground mb-4 line-clamp-3">
									Everything you need to know about buying your first home in Charleston, from
									neighborhood selection to financing options and local programs.
								</p>
								<Button
									href="/blog/first-time-buyers-guide"
									variant="ghost"
									class="text-primary hover:text-primary/80 h-auto p-0"
								>
									Read More →
								</Button>
							</div>
						</CardContent>
					</Card>

					<!-- Blog Post 2 -->
					<Card class="border-primary/20 transition-all hover:scale-105 hover:shadow-lg">
						<CardContent class="p-0">
							<!-- Featured Image -->
							<div class="h-48 overflow-hidden">
								<img
									src={mtPleasant}
									alt="Mount Pleasant, Charleston"
									class="h-full w-full object-cover transition-transform duration-300 hover:scale-105"
								/>
							</div>
							<div class="p-6">
								<div class="text-muted-foreground mb-2 flex items-center space-x-2 text-sm">
									<span>October 10, 2025</span>
									<span>•</span>
									<span>7 min read</span>
								</div>
								<h3 class="text-foreground mb-3 line-clamp-2 text-xl font-semibold">
									Mount Pleasant vs West Ashley: A Local's Perspective
								</h3>
								<p class="text-muted-foreground mb-4 line-clamp-3">
									Comparing Charleston's most popular neighborhoods to help you decide where to call
									home based on lifestyle, amenities, and value.
								</p>
								<Button
									href="/blog/mount-pleasant-vs-west-ashley"
									variant="ghost"
									class="text-primary hover:text-primary/80 h-auto p-0"
								>
									Read More →
								</Button>
							</div>
						</CardContent>
					</Card>

					<!-- Blog Post 3 -->
					<Card class="border-primary/20 transition-all hover:scale-105 hover:shadow-lg">
						<CardContent class="p-0">
							<!-- Featured Image -->
							<div class="h-48 overflow-hidden">
								<img
									src={rainbowRow}
									alt="Rainbow Row, Charleston"
									class="h-full w-full object-cover transition-transform duration-300 hover:scale-105"
								/>
							</div>
							<div class="p-6">
								<div class="text-muted-foreground mb-2 flex items-center space-x-2 text-sm">
									<span>October 5, 2025</span>
									<span>•</span>
									<span>4 min read</span>
								</div>
								<h3 class="text-foreground mb-3 line-clamp-2 text-xl font-semibold">
									October 2025 Charleston Market Update
								</h3>
								<p class="text-muted-foreground mb-4 line-clamp-3">
									Current market trends, pricing insights, and what buyers and sellers can expect in
									the Charleston real estate market this fall.
								</p>
								<Button
									href="/blog/october-2025-market-update"
									variant="ghost"
									class="text-primary hover:text-primary/80 h-auto p-0"
								>
									Read More →
								</Button>
							</div>
						</CardContent>
					</Card>
				</div>

				<div class="mt-8 text-center">
					<Button
						href="/blog"
						variant="outline"
						size="lg"
						class="border-primary/20 hover:border-primary/40"
					>
						Read All Articles
					</Button>
				</div>
			</div>

			<!-- Testimonials Section -->
			<div class="mt-20">
				<div class="mb-12 text-center">
					<h2 class="text-foreground text-3xl font-bold md:text-4xl">What Clients Say</h2>
					<p class="text-muted-foreground mx-auto mt-4 max-w-2xl text-lg">
						Don't just take our word for it. Here's what our clients have to say about their
						Charleston real estate experience.
					</p>
				</div>

				<div class="grid grid-cols-1 gap-8 md:grid-cols-2">
					<!-- Testimonial 1 -->
					<Card class="border-primary/20 bg-background/50 backdrop-blur-sm">
						<CardContent class="p-8">
							<div class="mb-4 flex items-center space-x-1">
								<!-- 5 Star Rating -->
								{#each Array(5) as _}
									<svg class="h-5 w-5 fill-current text-yellow-400" viewBox="0 0 20 20">
										<path
											d="M10 15l-5.878 3.09 1.123-6.545L.489 6.91l6.572-.955L10 0l2.939 5.955 6.572.955-4.756 4.635 1.123 6.545z"
										/>
									</svg>
								{/each}
							</div>
							<blockquote class="text-muted-foreground mb-6 text-lg italic">
								"Kai made our first home buying experience in Charleston absolutely seamless. His
								knowledge of the local neighborhoods helped us find the perfect place in Mount
								Pleasant. We couldn't be happier!"
							</blockquote>
							<div class="flex items-center space-x-4">
								<div class="bg-primary/10 flex h-12 w-12 items-center justify-center rounded-full">
									<svg
										class="text-primary h-6 w-6"
										fill="none"
										stroke="currentColor"
										viewBox="0 0 24 24"
									>
										<path
											stroke-linecap="round"
											stroke-linejoin="round"
											stroke-width="2"
											d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z"
										></path>
									</svg>
								</div>
								<div>
									<div class="text-foreground font-semibold">Sarah & Mike Johnson</div>
									<div class="text-muted-foreground text-sm">Mount Pleasant, SC</div>
								</div>
							</div>
						</CardContent>
					</Card>

					<!-- Testimonial 2 -->
					<Card class="border-primary/20 bg-background/50 backdrop-blur-sm">
						<CardContent class="p-8">
							<div class="mb-4 flex items-center space-x-1">
								<!-- 5 Star Rating -->
								{#each Array(5) as _}
									<svg class="h-5 w-5 fill-current text-yellow-400" viewBox="0 0 20 20">
										<path
											d="M10 15l-5.878 3.09 1.123-6.545L.489 6.91l6.572-.955L10 0l2.939 5.955 6.572.955-4.756 4.635 1.123 6.545z"
										/>
									</svg>
								{/each}
							</div>
							<blockquote class="text-muted-foreground mb-6 text-lg italic">
								"Professional, knowledgeable, and genuinely caring. Kai helped us sell our downtown
								Charleston home quickly and for a great price. His market expertise is unmatched."
							</blockquote>
							<div class="flex items-center space-x-4">
								<div class="bg-primary/10 flex h-12 w-12 items-center justify-center rounded-full">
									<svg
										class="text-primary h-6 w-6"
										fill="none"
										stroke="currentColor"
										viewBox="0 0 24 24"
									>
										<path
											stroke-linecap="round"
											stroke-linejoin="round"
											stroke-width="2"
											d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z"
										></path>
									</svg>
								</div>
								<div>
									<div class="text-foreground font-semibold">Robert & Lisa Chen</div>
									<div class="text-muted-foreground text-sm">Downtown Charleston, SC</div>
								</div>
							</div>
						</CardContent>
					</Card>
				</div>
			</div>

			<!-- Final CTA Section -->
			<div class="mt-20">
				<Card class="border-primary/20 from-primary/5 to-primary/10 bg-gradient-to-br">
					<CardContent class="p-12 text-center">
						<h2 class="text-foreground mb-4 text-3xl font-bold md:text-4xl">
							Ready to Start Your Charleston Real Estate Journey?
						</h2>
						<p class="text-muted-foreground mx-auto mb-8 max-w-2xl text-xl">
							Whether you're buying your first home, selling your current property, or exploring
							investment opportunities, I'm here to guide you every step of the way.
						</p>
						<div class="flex flex-col justify-center gap-4 sm:flex-row">
							<Button href="/contact" size="lg" class="px-8 py-3 text-lg">Contact Me Today</Button>
							<Button
								href="/contact"
								variant="outline"
								size="lg"
								class="border-primary/20 hover:border-primary/40 px-8 py-3 text-lg"
							>
								Schedule Consultation
							</Button>
						</div>
					</CardContent>
				</Card>
			</div>
		</div>
	</div>
</div>

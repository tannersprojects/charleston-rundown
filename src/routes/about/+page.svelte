<script lang="ts">
	import { Button } from '$lib/components/ui/button';
	import { Card, CardContent } from '$lib/components/ui/card';
	import headshot from '$lib/assets/headshot.jpeg';
	import charlestonBattery from '$lib/assets/charleston-images/charleston-battery.jpg';
</script>

<svelte:head>
	<title>About Kai Fischer - Charleston Real Estate Agent</title>
	<meta
		name="description"
		content="Meet Kai Fischer, your trusted Charleston real estate expert with deep local knowledge and a passion for helping clients find their perfect home in the Lowcountry."
	/>
</svelte:head>

<div class="page-container">
	<div class="page-content-extra-wide">
		<div class="space-y-16">
			<!-- Hero Section -->
			<div class="space-y-6 text-center">
				<h1 class="text-foreground text-4xl font-bold tracking-tight md:text-5xl">
					Meet Kai Fischer
				</h1>
				<p class="text-muted-foreground mx-auto max-w-2xl text-xl">
					Your Trusted Charleston Real Estate Expert
				</p>
			</div>

			<!-- About Content -->
			<div class="grid grid-cols-1 gap-12 lg:grid-cols-2 lg:gap-16">
				<!-- Professional Headshot -->
				<div class="flex items-center justify-center">
					<div class="relative">
						<!-- Professional styling with shadow and border -->
						<div class="ring-primary/10 relative overflow-hidden rounded-2xl shadow-2xl ring-4">
							<img
								src={headshot}
								alt="Kai Fischer - Charleston Real Estate Agent"
								class="h-80 w-80 object-cover transition-transform duration-300 hover:scale-105 lg:h-96 lg:w-96"
								loading="eager"
							/>
							<!-- Subtle overlay for professional depth -->
							<div class="from-primary/5 absolute inset-0 bg-gradient-to-t to-transparent"></div>
						</div>
						<!-- Decorative elements -->
						<div class="bg-primary/10 absolute -bottom-4 -right-4 h-16 w-16 rounded-full"></div>
						<div class="bg-primary/5 absolute -left-4 -top-4 h-12 w-12 rounded-full"></div>
					</div>
				</div>

				<!-- Story Content -->
				<div class="space-y-6">
					<div>
						<h2 class="text-foreground mb-4 text-2xl font-semibold">My Story</h2>
						<p class="text-muted-foreground leading-relaxed">
							I fell in love with Charleston's charm and unique character years ago, and that
							passion drives everything I do as a real estate professional. My journey into real
							estate began with a desire to help others discover the magic of this incredible city I
							now call home.
						</p>
					</div>

					<div>
						<h3 class="text-foreground mb-3 text-xl font-semibold">Why Charleston?</h3>
						<p class="text-muted-foreground leading-relaxed">
							Charleston isn't just a place to live—it's a lifestyle. From the historic downtown
							charm to the family-friendly suburbs, from the pristine beaches to the vibrant
							culinary scene, there's something special here for everyone. I love helping clients
							find their perfect corner of this amazing city.
						</p>
					</div>

					<div>
						<h3 class="text-foreground mb-3 text-xl font-semibold">My Approach</h3>
						<p class="text-muted-foreground leading-relaxed">
							I believe that buying or selling a home should be an exciting journey, not a stressful
							experience. My approach is built on clear communication, local expertise, and genuine
							care for my clients' goals. I'm here to guide you through every step of the process
							with patience, professionalism, and a deep understanding of what makes Charleston
							special.
						</p>
					</div>
				</div>
			</div>

			<!-- Charleston Connection Section -->
			<div class="relative overflow-hidden rounded-2xl shadow-2xl">
				<!-- Background Image -->
				<div class="absolute inset-0">
					<img
						src={charlestonBattery}
						alt="Charleston Battery"
						class="h-full w-full object-cover"
						loading="lazy"
					/>
					<!-- Overlay for text readability -->
					<div class="absolute inset-0 bg-black/50"></div>
				</div>

				<!-- Content -->
				<div class="relative px-8 py-16 text-center text-white md:px-12 md:py-20">
					<h2 class="text-3xl font-bold tracking-tight md:text-4xl">Deep Charleston Roots</h2>
					<p class="mx-auto mt-6 max-w-2xl text-lg text-white/90 md:text-xl">
						Born and raised in the Lowcountry, I understand Charleston's unique charm, historic
						neighborhoods, and what makes this city such a special place to call home.
					</p>
					<div class="mt-8 flex justify-center">
						<Button href="/blog" variant="outline" size="lg" class="border-black/20 text-black">
							Explore Charleston Neighborhoods
						</Button>
					</div>
				</div>
			</div>

			<!-- Credentials Section -->
			<Card class="border-primary/20 bg-background/50 backdrop-blur-sm">
				<CardContent class="p-8">
					<h2 class="text-foreground mb-6 text-center text-2xl font-semibold">
						Professional Credentials
					</h2>
					<div class="grid grid-cols-1 gap-6 md:grid-cols-2">
						<div class="text-center">
							<div
								class="bg-primary/10 mx-auto mb-4 flex h-16 w-16 items-center justify-center rounded-full"
							>
								<svg
									class="text-primary h-8 w-8"
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
							<h3 class="text-foreground mb-2 text-lg font-semibold">License</h3>
							<p class="text-muted-foreground">#123456789</p>
						</div>
						<div class="text-center">
							<div
								class="bg-primary/10 mx-auto mb-4 flex h-16 w-16 items-center justify-center rounded-full"
							>
								<svg
									class="text-primary h-8 w-8"
									fill="none"
									stroke="currentColor"
									viewBox="0 0 24 24"
								>
									<path
										stroke-linecap="round"
										stroke-linejoin="round"
										stroke-width="2"
										d="M19 21V5a2 2 0 00-2-2H7a2 2 0 00-2 2v16m14 0h2m-2 0h-5m-9 0H3m2 0h5M9 7h1m-1 4h1m4-4h1m-1 4h1m-5 10v-5a1 1 0 011-1h2a1 1 0 011 1v5m-4 0h4"
									></path>
								</svg>
							</div>
							<h3 class="text-foreground mb-2 text-lg font-semibold">Brokerage</h3>
							<p class="text-muted-foreground">Lively Real Estate, LLC</p>
						</div>
					</div>
				</CardContent>
			</Card>

			<!-- Values Section -->
			<div class="space-y-8 text-center">
				<h2 class="text-foreground text-2xl font-semibold">My Commitment to You</h2>
				<div class="grid grid-cols-1 gap-8 md:grid-cols-3">
					<Card class="border-primary/20 transition-shadow hover:shadow-lg">
						<CardContent class="p-6 text-center">
							<div
								class="bg-primary/10 mx-auto mb-4 flex h-12 w-12 items-center justify-center rounded-full"
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
										d="M13 10V3L4 14h7v7l9-11h-7z"
									></path>
								</svg>
							</div>
							<h3 class="text-foreground mb-2 text-lg font-semibold">Fast Response</h3>
							<p class="text-muted-foreground text-sm">
								I respond to all inquiries within hours, not days. Your time is valuable, and I
								respect that.
							</p>
						</CardContent>
					</Card>

					<Card class="border-primary/20 transition-shadow hover:shadow-lg">
						<CardContent class="p-6 text-center">
							<div
								class="bg-primary/10 mx-auto mb-4 flex h-12 w-12 items-center justify-center rounded-full"
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
										d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z"
									></path>
								</svg>
							</div>
							<h3 class="text-foreground mb-2 text-lg font-semibold">Trust & Integrity</h3>
							<p class="text-muted-foreground text-sm">
								Honest advice and transparent communication are the foundation of every client
								relationship.
							</p>
						</CardContent>
					</Card>

					<Card class="border-primary/20 transition-shadow hover:shadow-lg">
						<CardContent class="p-6 text-center">
							<div
								class="bg-primary/10 mx-auto mb-4 flex h-12 w-12 items-center justify-center rounded-full"
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
										d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"
									></path>
									<path
										stroke-linecap="round"
										stroke-linejoin="round"
										stroke-width="2"
										d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"
									></path>
								</svg>
							</div>
							<h3 class="text-foreground mb-2 text-lg font-semibold">Local Expertise</h3>
							<p class="text-muted-foreground text-sm">
								Deep knowledge of Charleston neighborhoods, market trends, and what makes each area
								special.
							</p>
						</CardContent>
					</Card>
				</div>
			</div>

			<!-- CTA Section -->
			<div class="text-center">
				<Card class="border-primary/20 from-primary/5 to-primary/10 bg-gradient-to-br">
					<CardContent class="p-8">
						<h2 class="text-foreground mb-4 text-2xl font-bold">Ready to Work Together?</h2>
						<p class="text-muted-foreground mx-auto mb-6 max-w-2xl">
							Let's discuss your real estate goals and how I can help you achieve them in
							Charleston's vibrant market.
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

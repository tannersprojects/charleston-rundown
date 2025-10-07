<script lang="ts">
	import { Button } from '$lib/components/ui/button';
	import { Card, CardContent } from '$lib/components/ui/card';
</script>

<svelte:head>
	<title>Properties - Charleston Real Estate | Kai Fischer</title>
	<meta
		name="description"
		content="Browse Charleston real estate properties with Kai Fischer. Find your perfect home in Charleston, Mount Pleasant, West Ashley, and surrounding areas."
	/>
</svelte:head>

<div class="page-container">
	<div class="page-content-extra-wide">
		<div class="space-y-16">
			<!-- Hero Section -->
			<div class="space-y-6 text-center">
				<h1 class="text-4xl font-bold tracking-tight text-foreground md:text-5xl">
					Charleston Properties
				</h1>
				<p class="mx-auto max-w-2xl text-xl text-muted-foreground">
					Discover your perfect home in Charleston. Browse our curated selection of properties
					across the Lowcountry.
				</p>
			</div>

			<!-- Coming Soon Card -->
			<div class="flex justify-center">
				<Card class="max-w-2xl border-primary/20 bg-gradient-to-br from-primary/5 to-primary/10">
					<CardContent class="p-12 text-center">
						<div
							class="mx-auto mb-6 flex h-24 w-24 items-center justify-center rounded-full bg-primary/10"
						>
							<svg
								class="h-12 w-12 text-primary"
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
						<h2 class="mb-4 text-3xl font-bold text-foreground">Property Search Coming Soon</h2>
						<p class="mx-auto mb-8 max-w-lg text-muted-foreground">
							We're building an advanced property search system with real-time MLS data. In the
							meantime, I can help you find the perfect property through direct consultation.
						</p>
						<div class="flex flex-col justify-center gap-4 sm:flex-row">
							<Button href="/contact" size="lg" class="px-8 py-3 text-lg">Contact Me Today</Button>
							<Button
								href="/contact"
								variant="outline"
								size="lg"
								class="border-primary/20 px-8 py-3 text-lg hover:border-primary/40"
							>
								Schedule Consultation
							</Button>
						</div>
					</CardContent>
				</Card>
			</div>

			<!-- Services Section -->
			<div class="space-y-8">
				<div class="text-center">
					<h2 class="text-3xl font-bold text-foreground md:text-4xl">How I Can Help You</h2>
					<p class="mx-auto mt-4 max-w-2xl text-lg text-muted-foreground">
						While we build our property search, I'm here to help you find your perfect Charleston
						home.
					</p>
				</div>

				<div class="grid grid-cols-1 gap-8 md:grid-cols-3">
					<Card class="border-primary/20 transition-shadow hover:shadow-lg">
						<CardContent class="p-6 text-center">
							<div
								class="mx-auto mb-4 flex h-12 w-12 items-center justify-center rounded-full bg-primary/10"
							>
								<svg
									class="h-6 w-6 text-primary"
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
							<h3 class="mb-2 text-lg font-semibold text-foreground">Custom Property Search</h3>
							<p class="text-sm text-muted-foreground">
								I'll search the MLS for properties that match your exact criteria and preferences.
							</p>
						</CardContent>
					</Card>

					<Card class="border-primary/20 transition-shadow hover:shadow-lg">
						<CardContent class="p-6 text-center">
							<div
								class="mx-auto mb-4 flex h-12 w-12 items-center justify-center rounded-full bg-primary/10"
							>
								<svg
									class="h-6 w-6 text-primary"
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
							<h3 class="mb-2 text-lg font-semibold text-foreground">Neighborhood Expertise</h3>
							<p class="text-sm text-muted-foreground">
								Get insider knowledge about Charleston neighborhoods, schools, and local amenities.
							</p>
						</CardContent>
					</Card>

					<Card class="border-primary/20 transition-shadow hover:shadow-lg">
						<CardContent class="p-6 text-center">
							<div
								class="mx-auto mb-4 flex h-12 w-12 items-center justify-center rounded-full bg-primary/10"
							>
								<svg
									class="h-6 w-6 text-primary"
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
							<h3 class="mb-2 text-lg font-semibold text-foreground">Guided Tours</h3>
							<p class="text-sm text-muted-foreground">
								Schedule property tours and get expert guidance throughout your home buying journey.
							</p>
						</CardContent>
					</Card>
				</div>
			</div>
		</div>
	</div>
</div>

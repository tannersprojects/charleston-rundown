<script lang="ts">
	import { Button } from '$lib/components/ui/button';
	import { Card, CardContent } from '$lib/components/ui/card';
</script>

<div class="flex flex-1 items-center justify-center bg-gradient-to-br from-background to-muted/20">
	<div class="container mx-auto max-w-4xl px-4 sm:px-6 lg:px-8">
		<div class="space-y-8 text-center">
			<!-- Hero Section -->
			<div class="space-y-4">
				<h1 class="text-4xl font-bold tracking-tight text-foreground md:text-6xl">
					Welcome to
					<span class="text-primary">Charleston</span>
				</h1>
				<p class="mx-auto max-w-2xl text-xl text-muted-foreground md:text-2xl">
					Your premier destination for real estate in the beautiful Charleston area. Find your dream
					home with expert guidance.
				</p>
			</div>

			<!-- CTA Buttons -->
			<div class="flex flex-col justify-center gap-4 sm:flex-row">
				<Button size="lg" class="px-8 py-3 text-lg">View Properties</Button>
				<Button variant="outline" size="lg" class="px-8 py-3 text-lg">Schedule Consultation</Button>
			</div>

			<!-- Feature Cards -->
			<div class="mt-16 grid grid-cols-1 gap-6 md:grid-cols-3">
				<Card class="border-primary/20 transition-shadow hover:shadow-lg">
					<CardContent class="space-y-3 p-6 text-center">
						<div
							class="mx-auto flex h-12 w-12 items-center justify-center rounded-full bg-primary/10"
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
									d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6"
								></path>
							</svg>
						</div>
						<h3 class="text-lg font-semibold">Expert Guidance</h3>
						<p class="text-sm text-muted-foreground">
							Professional real estate expertise to guide you through every step
						</p>
					</CardContent>
				</Card>

				<Card class="border-primary/20 transition-shadow hover:shadow-lg">
					<CardContent class="space-y-3 p-6 text-center">
						<div
							class="mx-auto flex h-12 w-12 items-center justify-center rounded-full bg-primary/10"
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
						<h3 class="text-lg font-semibold">Prime Locations</h3>
						<p class="text-sm text-muted-foreground">
							Access to the best properties in Charleston's most desirable neighborhoods
						</p>
					</CardContent>
				</Card>

				<Card class="border-primary/20 transition-shadow hover:shadow-lg">
					<CardContent class="space-y-3 p-6 text-center">
						<div
							class="mx-auto flex h-12 w-12 items-center justify-center rounded-full bg-primary/10"
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
						<h3 class="text-lg font-semibold">Trusted Service</h3>
						<p class="text-sm text-muted-foreground">
							Dedicated support throughout your real estate journey
						</p>
					</CardContent>
				</Card>
			</div>
		</div>
	</div>
</div>

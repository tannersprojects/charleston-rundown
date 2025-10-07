<script lang="ts">
	import { Button } from '$lib/components/ui/button';
	import { Card, CardContent } from '$lib/components/ui/card';
	import { Input } from '$lib/components/ui/input';
	import { Textarea } from '$lib/components/ui/textarea';
	import { Label } from '$lib/components/ui/label';
	import { Alert, AlertDescription } from '$lib/components/ui/alert';
	import { Mail, Phone, MapPin, Clock } from '@lucide/svelte';

	let formData = {
		name: '',
		email: '',
		phone: '',
		message: ''
	};

	let isSubmitting = false;
	let submitMessage = '';

	function handleSubmit() {
		isSubmitting = true;
		// Simulate form submission
		setTimeout(() => {
			isSubmitting = false;
			submitMessage = "Thank you for your message! I'll get back to you within 24 hours.";
			// Reset form
			formData = { name: '', email: '', phone: '', message: '' };
		}, 2000);
	}
</script>

<svelte:head>
	<title>Contact Kai Fischer - Charleston Real Estate Agent</title>
	<meta
		name="description"
		content="Get in touch with Kai Fischer, your Charleston real estate expert. Contact form, phone number, email, and office location for all your real estate needs."
	/>
</svelte:head>

<div class="page-container">
	<div class="page-content-extra-wide">
		<div class="space-y-12">
			<!-- Hero Section -->
			<div class="space-y-4 text-center">
				<h1 class="text-4xl font-bold tracking-tight text-foreground md:text-5xl">Get In Touch</h1>
				<p class="mx-auto max-w-2xl text-xl text-muted-foreground">
					Ready to start your Charleston real estate journey? I'm here to help make it seamless and
					successful.
				</p>
			</div>

			<!-- Contact Content - Restructured Layout -->
			<div class="grid grid-cols-1 gap-6 lg:grid-cols-2 lg:items-stretch">
				<!-- Left Column -->
				<div class="flex flex-col space-y-6">
					<!-- Contact Form -->
					<Card class="flex-[2] border-primary/20 bg-background/50 backdrop-blur-sm">
						<CardContent class="flex h-full flex-col p-6">
							<h2 class="mb-4 text-xl font-semibold text-foreground">Send a Message</h2>

							{#if submitMessage}
								<Alert class="mb-4">
									<AlertDescription>{submitMessage}</AlertDescription>
								</Alert>
							{/if}

							<form on:submit|preventDefault={handleSubmit} class="flex flex-1 flex-col space-y-4">
								<div class="grid grid-cols-1 gap-4 md:grid-cols-2">
									<div class="space-y-2">
										<Label for="name">Name *</Label>
										<Input
											type="text"
											id="name"
											bind:value={formData.name}
											required
											placeholder="Your full name"
										/>
									</div>

									<div class="space-y-2">
										<Label for="email">Email *</Label>
										<Input
											type="email"
											id="email"
											bind:value={formData.email}
											required
											placeholder="your.email@example.com"
										/>
									</div>
								</div>

								<div class="space-y-2">
									<Label for="phone">Phone</Label>
									<Input
										type="tel"
										id="phone"
										bind:value={formData.phone}
										placeholder="(555) 555-5555"
									/>
								</div>

								<div class="flex flex-1 flex-col space-y-2">
									<Label for="message">Message *</Label>
									<Textarea
										class="flex-1 resize-none"
										id="message"
										bind:value={formData.message}
										required
										placeholder="Tell me about your real estate goals..."
									/>
								</div>

								<Button type="submit" size="lg" class="w-full" disabled={isSubmitting}>
									{isSubmitting ? 'Sending...' : 'Send Message'}
								</Button>
							</form>
						</CardContent>
					</Card>

					<!-- Call to Action -->
					<Card class="flex-1 border-primary/20 bg-gradient-to-br from-primary/5 to-primary/10">
						<CardContent class="flex h-full flex-col justify-center p-8">
							<h2 class="mb-3 text-lg font-bold text-foreground">Prefer to Talk Directly?</h2>
							<p class="mb-6 text-sm leading-relaxed text-muted-foreground">
								Sometimes a quick phone call is the best way to get started. I'm always happy to
								chat about your real estate needs, answer questions, or schedule a time to meet.
							</p>
							<Button href="tel:(555) 555-5555" size="lg" class="w-full">
								Call (555) 555-5555
							</Button>
						</CardContent>
					</Card>
				</div>

				<!-- Right Column -->
				<div class="flex flex-col space-y-6">
					<!-- Direct Contact -->
					<Card class="border-primary/20 bg-background/50 backdrop-blur-sm">
						<CardContent class="p-6">
							<h2 class="mb-4 text-xl font-semibold text-foreground">Direct Contact</h2>
							<div class="space-y-4">
								<div class="flex items-center space-x-4">
									<div
										class="flex h-12 w-12 items-center justify-center rounded-full bg-primary/10"
									>
										<Phone class="h-6 w-6 text-primary" />
									</div>
									<div>
										<h3 class="text-sm font-semibold text-foreground">Phone</h3>
										<a
											href="tel:(555) 555-5555"
											class="text-base text-muted-foreground transition-colors hover:text-primary"
										>
											(555) 555-5555
										</a>
									</div>
								</div>

								<div class="flex items-center space-x-4">
									<div
										class="flex h-12 w-12 items-center justify-center rounded-full bg-primary/10"
									>
										<Mail class="h-6 w-6 text-primary" />
									</div>
									<div>
										<h3 class="text-sm font-semibold text-foreground">Email</h3>
										<a
											href="mailto:kaifischer@livelyrealestate.com"
											class="text-base text-muted-foreground transition-colors hover:text-primary"
										>
											kaifischer@livelyrealestate.com
										</a>
									</div>
								</div>

								<div class="flex items-center space-x-4">
									<div
										class="flex h-12 w-12 items-center justify-center rounded-full bg-primary/10"
									>
										<Clock class="h-6 w-6 text-primary" />
									</div>
									<div>
										<h3 class="text-sm font-semibold text-foreground">Response Time</h3>
										<p class="text-base text-muted-foreground">Within 24 hours</p>
									</div>
								</div>
							</div>
						</CardContent>
					</Card>

					<!-- Office Information -->
					<Card class="border-primary/20 bg-background/50 backdrop-blur-sm">
						<CardContent class="p-6">
							<h2 class="mb-4 text-xl font-semibold text-foreground">Office Location</h2>
							<div class="flex items-start space-x-4">
								<div class="flex h-12 w-12 items-center justify-center rounded-full bg-primary/10">
									<MapPin class="h-6 w-6 text-primary" />
								</div>
								<div>
									<h3 class="mb-2 font-semibold text-foreground">Lively Real Estate, LLC</h3>
									<p class="text-sm text-muted-foreground">
										[Office Address]<br />
										Charleston, SC 29401<br /><br />
										<strong>Office Hours:</strong><br />
										Monday - Friday: 9:00 AM - 6:00 PM<br />
										Saturday: 10:00 AM - 4:00 PM<br />
										Sunday: By Appointment
									</p>
								</div>
							</div>
						</CardContent>
					</Card>

					<!-- Map Placeholder -->
					<Card class="flex-1 border-primary/20 bg-background/50 backdrop-blur-sm">
						<CardContent class="flex h-full flex-col p-6">
							<h2 class="mb-4 text-xl font-semibold text-foreground">Find Us</h2>
							<div class="flex flex-1 items-center justify-center rounded-md bg-primary/10">
								<div class="text-center">
									<MapPin class="mx-auto mb-2 h-10 w-10 text-primary" />
									<p class="text-sm font-medium text-muted-foreground">Google Maps Integration</p>
									<p class="text-xs text-muted-foreground">Interactive map will be added here</p>
								</div>
							</div>
						</CardContent>
					</Card>
				</div>
			</div>
		</div>
	</div>
</div>

<script lang="ts">
	import '../app.css';
	import favicon from '$lib/assets/favicon.svg';
	import { Button } from '$lib/components/ui/button';
	import { Sheet, SheetContent, SheetHeader, SheetTrigger } from '$lib/components/ui/sheet';
	import { Menu, House, User, SquarePen, Mail, Linkedin, Instagram } from '@lucide/svelte';

	let { children } = $props();

	let open = $state(false);

	const navLinks = [
		{ href: '/', label: 'Home', icon: House },
		{ href: '/about', label: 'About', icon: User },
		{ href: '/blog', label: 'Blog', icon: SquarePen },
		{ href: '/contact', label: 'Contact', icon: Mail }
	];

	const name = 'Kai Fischer';
	const brokerageName = 'Lively Real Estate';
	const licenseNumber = '123456789';
	const phoneNumber = '(555) 555-5555';
	const email = 'kaifischer@livelyrealestate.com';
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

<div class="flex min-h-screen flex-col bg-background text-foreground">
	<header
		class="sticky top-0 z-50 w-full border-b bg-background/95 shadow-sm backdrop-blur supports-[backdrop-filter]:bg-background/60"
	>
		<nav
			class="container mx-auto flex h-16 max-w-7xl items-center justify-between px-4 sm:px-6 lg:px-8"
		>
			<a href="/" class="text-xl font-bold text-primary transition-colors hover:text-primary/80"
				>{name} | RE</a
			>

			<div class="hidden items-center space-x-6 md:flex">
				{#each navLinks as link}
					<a href={link.href} class="transition-colors hover:text-primary">
						<Button variant="ghost" class="text-sm font-medium">{link.label}</Button>
					</a>
				{/each}
			</div>

			<div class="md:hidden">
				<Sheet bind:open>
					<SheetTrigger>
						<Button variant="outline" size="icon" class="border-primary/20">
							<Menu class="h-5 w-5" />
							<span class="sr-only">Open menu</span>
						</Button>
					</SheetTrigger>
					<SheetContent class="w-[300px] sm:w-[400px]">
						<SheetHeader class="space-y-3">
							<a href="/" class="text-xl font-bold text-primary">Your Name | RE</a>
						</SheetHeader>
						<div class="mt-6 flex flex-col space-y-3">
							{#each navLinks as link}
								<a href={link.href} onclick={() => (open = false)} class="block">
									<Button variant="ghost" class="h-12 w-full justify-start space-x-3 text-left">
										<link.icon class="h-5 w-5" />
										<span class="font-medium">{link.label}</span>
									</Button>
								</a>
							{/each}
						</div>
					</SheetContent>
				</Sheet>
			</div>
		</nav>
	</header>

	<main class="flex flex-1 flex-col">
		{@render children()}
	</main>

	<footer class="w-full border-t bg-muted/30 shadow-sm">
		<div class="container mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
			<div class="grid grid-cols-1 gap-8 py-12 md:grid-cols-3">
				<div class="flex flex-col items-center gap-3 text-center">
					<h3 class="text-lg font-semibold text-foreground">{name}</h3>
					<p class="text-sm text-muted-foreground">{brokerageName}, LLC</p>
					<p class="text-sm text-muted-foreground">License #{licenseNumber}</p>
				</div>
				<div class="flex flex-col items-center gap-3 text-center">
					<h3 class="text-lg font-semibold text-foreground">Contact</h3>
					<a
						href="tel:{phoneNumber}"
						class="text-sm text-muted-foreground transition-colors hover:text-primary"
						>{phoneNumber}</a
					>
					<a
						href="mailto:{email}"
						class="text-sm text-muted-foreground transition-colors hover:text-primary"
					>
						{email}
					</a>
				</div>
				<div class="flex flex-col items-center gap-3 text-center">
					<h3 class="text-lg font-semibold text-foreground">Follow</h3>
					<div class="flex items-center justify-center space-x-3">
						<a href="#linkedin" class="transition-transform hover:scale-105">
							<Button
								variant="outline"
								size="icon"
								class="border-primary/20 hover:border-primary/40"
							>
								<Linkedin class="h-4 w-4" />
							</Button>
						</a>
						<a href="#instagram" class="transition-transform hover:scale-105">
							<Button
								variant="outline"
								size="icon"
								class="border-primary/20 hover:border-primary/40"
							>
								<Instagram class="h-4 w-4" />
							</Button>
						</a>
					</div>
				</div>
			</div>
			<div class="border-t border-border/50 py-6">
				<p class="text-center text-sm text-muted-foreground">
					© {new Date().getFullYear()}
					{name}. All Rights Reserved.
				</p>
			</div>
		</div>
	</footer>
</div>

<script lang="ts">
	import { Button } from '$lib/components/ui/button/index.js';
	import * as Card from '$lib/components/ui/card/index.js';
	import { Input } from '$lib/components/ui/input/index.js';
	import { Label } from '$lib/components/ui/label/index.js';
	import { Checkbox } from '$lib/components/ui/checkbox/index.js';
	import Sun from 'svelte-radix/Sun.svelte';
	import Moon from 'svelte-radix/Moon.svelte';
	import GithubLogo from 'svelte-radix/GithubLogo.svelte';
	import LinkedinLogo from 'svelte-radix/LinkedinLogo.svelte';
	import { toggleMode } from 'mode-watcher';

	const frameworks = [
		{
			value: 'sveltekit',
			label: 'SvelteKit'
		},
		{
			value: 'next',
			label: 'Next.js'
		},
		{
			value: 'astro',
			label: 'Astro'
		},
		{
			value: 'nuxt',
			label: 'Nuxt.js'
		}
	];
	let checked = false;
	let email = '';
	let password = '';
</script>

<!-- Toggle Light and Dark modes -->
<div class="md:container md:mx-auto">
	<div class="flex justify-end">
		<Button on:click={toggleMode} variant="outline" size="icon">
			<Sun
				class="h-[1.2rem] w-[1.2rem] rotate-0 scale-100 transition-all dark:-rotate-90 dark:scale-0"
			/>
			<Moon
				class="absolute h-[1.2rem] w-[1.2rem] rotate-90 scale-0 transition-all dark:rotate-0 dark:scale-100"
			/>
			<span class="sr-only">Toggle theme</span>
		</Button>
	</div>
	<!-- Card component -->
	<Card.Root class="w-[350px]">
		<Card.Header class="space-y-1">
			<Card.Title class="text-2xl">Create an account</Card.Title>
			<Card.Description>Enter your email below to create your account</Card.Description>
		</Card.Header>
		<Card.Content class="grid gap-4">
			<div class="grid grid-cols-2 gap-6">
				<Button variant="outline">
					<GithubLogo class="mr-2 h-4 w-4" />
					GitHub
				</Button>
				<Button variant="outline">
					<LinkedinLogo class="mr-2 h-4 w-4" />
					LinkedIn
				</Button>
			</div>
			<div class="relative">
				<div class="absolute inset-0 flex items-center">
					<span class="w-full border-t" />
				</div>
				<div class="relative flex justify-center text-xs uppercase">
					<span class="bg-card px-2 text-muted-foreground"> Or continue with </span>
				</div>
			</div>
			<div class="grid gap-2">
				<Label for="email">Email</Label>
				<Input id="email" type="email" placeholder="me@example.com" bind:value={email} />
			</div>
			<div class="grid gap-2">
				<Label for="password">Password</Label>
				<Input id="password" type="password" bind:value={password} />
			</div>
			<div class="flex items-center space-x-2">
				<Checkbox id="terms" bind:checked />
				<Label
					for="terms"
					class="text-sm font-medium leading-none peer-disabled:cursor-not-allowed peer-disabled:opacity-70"
				>
					Accept terms and conditions
				</Label>
			</div>
		</Card.Content>
		<Card.Footer>
			<Button class="w-full" disabled={!checked}>Create account</Button>
		</Card.Footer>
	</Card.Root>
</div>

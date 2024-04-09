<script lang="ts">
	import { Button } from '$lib/components/ui/button/index.js';
	import EnvelopeOpen from 'svelte-radix/EnvelopeOpen.svelte';
	import ChevronRight from 'svelte-radix/ChevronRight.svelte';
	import Reload from 'svelte-radix/Reload.svelte';
</script>

<div class="container pt-6">
	<Button>Button</Button>
	<Button variant="secondary">Secondary</Button>
	<Button variant="destructive">Destructive</Button>
	<Button variant="outline">Outline</Button>
	<Button variant="ghost">Ghost</Button>
	<Button variant="link">Link</Button>
	<Button>
		<EnvelopeOpen class="mr-2 h-4 w-4" />
		Login with Email
	</Button>
	<Button variant="outline" size="icon">
		<ChevronRight class="h-4 w-4" />
	</Button>
	<Button disabled>
		<Reload class="mr-2 h-4 w-4 animate-spin" />
		Please wait
	</Button>
</div>

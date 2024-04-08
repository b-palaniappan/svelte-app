<script lang="ts">
	import { onMount } from 'svelte';
	import { Progress } from '$lib/components/ui/progress/index.js';

	let value = 13;
	onMount(() => {
		const timer = setTimeout(() => (value = 66), 500);
		return () => clearTimeout(timer);
	});
</script>

<div class="container pt-5">
	<Progress {value} max={100} class="w-[60%]" />
</div>

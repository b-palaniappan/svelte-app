<script lang="ts">
	import { toast } from 'svelte-sonner';
	import { Button } from '$lib/components/ui/button/index.js';
</script>

<!-- Not working. Figure it out. -->
<div class="container pt-5">
	<Button
		variant="outline"
		on:click={() =>
			toast.success('Event has been created', {
				description: 'Sunday, December 03, 2023 at 9:00 AM',
				action: {
					label: 'Undo',
					onClick: () => console.info('Undo')
				}
			})}
	>
		Show Toast
	</Button>
</div>

<script lang="ts">
	import { getLocalTimeZone, today } from '@internationalized/date';
	import { Calendar } from '$lib/components/ui/calendar/index.js';

	let value = today(getLocalTimeZone());
</script>

<div class="flex min-h-[350px] w-full items-center justify-center p-10">
	<Calendar bind:value class="rounded-md border shadow" />
</div>

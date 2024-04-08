<script lang="ts">
	import FontBold from 'svelte-radix/FontBold.svelte';
	import FontItalic from 'svelte-radix/FontItalic.svelte';
	import Underline from 'svelte-radix/Underline.svelte';
	import * as ToggleGroup from '$lib/components/ui/toggle-group/index.js';
	import { Toggle } from '$lib/components/ui/toggle/index.js';
</script>

<div class="container pt-5">
	<div>
		<Toggle aria-label="toggle bold">
			<FontBold class="h-4 w-4" />
		</Toggle>
	</div>
	<div>
		<ToggleGroup.Root type="multiple">
			<ToggleGroup.Item value="bold" aria-label="Toggle bold">
				<FontBold class="h-4 w-4" />
			</ToggleGroup.Item>
			<ToggleGroup.Item value="italic" aria-label="Toggle italic">
				<FontItalic class="h-4 w-4" />
			</ToggleGroup.Item>
			<ToggleGroup.Item value="strikethrough" aria-label="Toggle strikethrough">
				<Underline class="h-4 w-4" />
			</ToggleGroup.Item>
		</ToggleGroup.Root>
	</div>
</div>

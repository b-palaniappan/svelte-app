<script lang="ts">
	import '../app.pcss';
	import '@fontsource/poppins';
	import { ModeWatcher } from 'mode-watcher';
</script>

<!-- Toggle Light and Dark modes -->
<ModeWatcher />
<slot />

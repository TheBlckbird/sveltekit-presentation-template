<script lang="ts">
	import { onMount } from 'svelte'

	import Reveal from 'reveal.js'
	// import Highlight from 'reveal.js/plugin/highlight/highlight' // This is not included by default because it is almost 1MB in size
	import Markdown from 'reveal.js/plugin/markdown/markdown'
	import Notes from 'reveal.js/plugin/notes/notes'

	import 'reveal.js/dist/reveal.css'
	import 'reveal.js/dist/theme/black.css'
	import 'reveal.js/plugin/highlight/monokai.css'

	onMount(() => {
		const deck = new Reveal({
			plugins: [
				Markdown,
				// Highlight,
				Notes
			],
			autoAnimateEasing: 'ease',
			autoAnimateDuration: 1,
			hash: true,
			history: false,
			slideNumber: true,
			controls: false,
			navigationMode: 'linear'
			// progress: false
		})

		deck.initialize()
	})
</script>

<div class="reveal">
	<div class="slides">
		<slot />
	</div>
</div>

<script lang="ts">
	import Slide from '$lib/deck/Slide.svelte'
	import Markdown from '$lib/deck/Markdown.svelte'
	import Presentation from "$lib/deck/Presentation.svelte";
	import "../app.css"
</script>

<svelte:head>
	<title>My Presentation</title>
</svelte:head>

<Presentation>
	<Markdown>
		# This is markdown

		---

		And this is another slide

		--

		- and this a vertical with a list
		
		---

		1. And numbers
		2. And more numbers
		3. And even more numbers
	</Markdown>

	<!-- You can even include external Markdown files. Just put them into `static/file.md` or load them form a URL -->
	<Markdown file="slides.md" /> 

	<Slide>Horizontal Slide</Slide>

	<Slide>
		<Slide>Vertical Slide 1</Slide>
		<Slide>Vertical Slide 2</Slide>
	</Slide>

	<Slide animate>
		<ul>
			<li>React</li>
			<li>Solid</li>
			<li>Svelte</li>
			<li>Vue</li>
		</ul>
	</Slide>

	<Slide animate>
		<ul>
			<li>Svelte ❤️</li>
			<li>React</li>
			<li>Solid</li>
			<li>Vue</li>
		</ul>
	</Slide>
</Presentation>
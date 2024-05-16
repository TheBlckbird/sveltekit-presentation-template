<script lang="ts">
	export let file: string | null = null
</script>

{#if file != null}
	<section data-markdown={file} data-separator="---\n" data-separator-vertical="--\n" />
{:else}
	<section data-markdown data-separator="---\n" data-separator-vertical="--\n">
		<div data-template>
			<slot />
		</div>
	</section>
{/if}

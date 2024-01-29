<script lang="ts">
	import { useFlag, useVariant } from '@unleash/proxy-client-svelte';

	const enabled = useFlag('svelte-test-feature');
	const variant = useVariant('svelte-test-feature');

	const customContextFlag = useFlag('custom-context-flag');

	$: console.table({ $enabled, $variant });
</script>

<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>

{#if $enabled}
	<p>New toggle is enabled</p>
	<p>Variant is {JSON.stringify($variant)}</p>
{:else}
	<p>New toggle is disabled</p>
{/if}

{#if $customContextFlag}
	<p>Custom context flag is enabled</p>
{:else}
	<p>Custom context flag is disabled</p>
{/if}

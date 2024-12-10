<script lang="ts">
	import { FlagProvider, type IConfig } from '@unleash/proxy-client-svelte';

	const config: IConfig = {
		url: 'https://app.unleash-hosted.com/demo/api/frontend',
		clientKey: 'svelte-demo:development.1b19ac66c94211d8f08148d0a68463b05503d37acd01b670160b04bf',
		refreshInterval: 2,
		appName: 'svelte-sdk-demo',
		context: {
			properties: {
				customContext: 'yes'
			}
		}
	};
</script>

<FlagProvider {config}>
	<slot />
</FlagProvider>

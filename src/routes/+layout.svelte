<script lang="ts">
	import { FlagProvider, type IConfig } from '@unleash/proxy-client-svelte';

	const config: IConfig = {
		url: 'https://app.unleash-hosted.com/demo/api/frontend',
		clientKey:
			'custom-context-test:default.dfb62cbcda870f2c6516e19dcf40ededd70799d7c9fe50c64e894a26',
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

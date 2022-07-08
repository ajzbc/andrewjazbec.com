<script lang="ts">
	import { Icon } from '@steeze-ui/svelte-icon';
	import { ExternalLink } from '@steeze-ui/heroicons';

	export let name: string;
	export let url: string;
</script>

<a
	href={url}
	target="_blank"
	class="group inline-flex items-center text-blue-500 hover:text-blue-600"
>
	<span class="text-3xl font-bold">{name}</span>
	<Icon
		src={ExternalLink}
		theme="solid"
		class="ml-1 h-8 w-8 scale-0 transition ease-in-out group-hover:scale-100 motion-reduce:transition-none"
	/>
</a>

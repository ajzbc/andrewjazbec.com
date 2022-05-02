<script lang="ts">
	import { Icon } from '@steeze-ui/svelte-icon';
	import { ExternalLink } from '@steeze-ui/heroicons';

	interface Project {
		name: string;
		link: string;
		description: string;
	}

	export let project: Project;
</script>

<div>
	<a
		href={project.link}
		target="_blank"
		class="group inline-flex items-center text-blue-500 hover:text-blue-600"
	>
		<h3 class="text-3xl font-bold">{project.name}</h3>
		<Icon
			src={ExternalLink}
			theme="solid"
			class="ml-1 h-8 w-8 scale-0 transition ease-in-out group-hover:scale-100 motion-reduce:transition-none"
		/>
	</a>
	<p class="text-xl text-slate-700">{project.description}</p>
</div>

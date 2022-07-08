<script lang="ts">
	import Link from './Link.svelte';
	interface Project {
		name: string;
		url: string;
		description: string;
	}

	export let project: Project;
</script>

<div>
	<Link name={project.name} url={project.url} />
	<p class="text-xl text-slate-700">{project.description}</p>
</div>

<script lang="ts">
	import { Icon } from '@steeze-ui/svelte-icon';
	import { Mail, Code } from '@steeze-ui/heroicons';

	import Link from '$lib/components/Link.svelte';

	import projects from '$lib/data/projects.json';
	import Project from '$lib/components/Project.svelte';

	import LastUpdated from '$lib/components/LastUpdated.svelte';
</script>

<header class="mt-6 mb-12">
	<h1 class="trackin mb-4 text-4xl font-extrabold sm:text-6xl">Andrew Jazbec</h1>

	<ul class="flex flex-col gap-2">
		<li>
			<Link name="Email" url="mailto:andrew@jazbec.io" />
		</li>
		<li>
			<Link name="GitHub" url="https://github.com/ajzbc" />
		</li>
	</ul>
</header>

<h2 class="mb-6 text-4xl font-extrabold sm:text-5xl">Projects</h2>

<ul class="flex flex-col gap-2">
	{#each projects as project}
		<li>
			<Project {project} />
		</li>
	{/each}
</ul>

<footer class="mt-auto flex flex-col justify-between pt-4 sm:flex-row">
	<p>Last updated <LastUpdated /></p>
	<a href="https://github.com/ajzbc/ajzbc.com" target="_blank">Source</a>
</footer>

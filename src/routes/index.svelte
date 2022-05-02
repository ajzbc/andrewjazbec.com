<script lang="ts">
	import { Icon } from '@steeze-ui/svelte-icon';
	import { Mail, Code } from '@steeze-ui/heroicons';

	import projects from '$lib/data/projects.json';
	import Project from '$lib/components/Project.svelte';

	import LastUpdated from '$lib/components/LastUpdated.svelte';
</script>

<header class="my-20">
	<h1 class="trackin mb-4 text-4xl font-extrabold text-slate-900 sm:text-6xl">Andrew Jazbec</h1>

	<ul class="inline-block">
		<li class="group">
			<a
				href="mailto:andrew@jazbec.io"
				class="flex items-center text-3xl font-semibold text-slate-700 group-hover:text-slate-800"
			>
				<Icon
					src={Mail}
					theme="outline"
					class="mr-3 inline h-10 w-10 text-green-500 transition ease-in-out group-hover:scale-110 motion-reduce:transition-none"
				/>
				Email
			</a>
		</li>
		<li class="group">
			<a
				href="https://github.com/ajzbc"
				class="flex items-center text-3xl font-semibold text-slate-700 group-hover:text-slate-800"
			>
				<Icon
					src={Code}
					theme="outline"
					class="mr-3 inline h-10 w-10 text-purple-500 transition ease-in-out group-hover:scale-110 motion-reduce:transition-none"
				/>
				GitHub
			</a>
		</li>
	</ul>
</header>

<h2 class="mb-6 text-4xl font-extrabold text-slate-900 sm:text-5xl">Projects</h2>

<div class="flex flex-col gap-4">
	{#each projects as project}
		<Project {project} />
	{/each}
</div>

<footer class="mt-auto flex flex-col justify-between pt-4 sm:flex-row">
	<p>Last updated <LastUpdated /></p>
	<a href="https://github.com/ajzbc/ajzbc.com">Source</a>
</footer>

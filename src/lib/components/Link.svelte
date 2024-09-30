<script lang="ts">
	import LinkedInIcon from './icons/LinkedInIcon.svelte';
	import LinkIcon from './icons/LinkIcon.svelte';
	import GithubIcon from './icons/GithubIcon.svelte';

	export let text: string;
	export let variant: 'site' | 'linkedin' | 'github';
	export let url: string;
</script>

<div
	class="flex antialiased items-center gap-2 transition ease-in-out hover:text-gray-400 hover:scale-110 duration-200"
>
	{#if variant === 'site'}
		<LinkIcon />
	{:else if variant === 'linkedin'}
		<LinkedInIcon />
	{:else if variant === 'github'}
		<GithubIcon />
	{/if}
	<a href={url} target="_blank" class="antialiased">{text}</a>
</div>

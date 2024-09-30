<script lang="ts">
	import LinkedInIcon from './icons/LinkedInIcon.svelte';
	import QuoteIcon from './icons/QuoteIcon.svelte';
	import Title from './Title.svelte';
	export let text: string;
	export let title: string;
	export let author: string;
	export let link: string | undefined = undefined;
</script>

<div class="bg-surface-700 bg-opacity-50 rounded-2xl p-8 flex flex-col">
	{#if link}
		<a
			href={link}
			target="_blank"
			class="hover:text-gray-500 transition ease-in-out duration-200 flex items-center gap-1 hover:scale-105"
		>
			<LinkedInIcon class="h-6 w-6" />
			<h4 class="h4">{author}</h4>
		</a>
	{:else}
		<h4 class="h4">{author}</h4>
	{/if}
	<Title>{title}</Title>
	<span class="flex my-4">
		<QuoteIcon class="flex-shrink-0" />
		<q class="italic text-wrap"> {text} </q>
	</span>
</div>

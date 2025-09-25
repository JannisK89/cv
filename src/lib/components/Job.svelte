<script lang="ts">
	import Title from '$lib/components/Title.svelte';

	export let title: string;
	export let company: string;
	export let from: string;
	export let to: string;
	export let description: string[];
  export let gap: boolean = true
</script>

<div>
	<h5 class="h5">{title}</h5>
	<Title>{company} | {from} - {to}</Title>
	<ul class="font-sans font-light text-sm antialiased list-inside">
		{#each description as item}
			<li class="list-disc {gap ? 'mb-4' : ''}">
				{item}
			</li>
		{/each}
	</ul>
</div>

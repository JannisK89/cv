<script lang="ts">
	import EmailIcon from './icons/EmailIcon.svelte';
	import LocationIcon from './icons/LocationIcon.svelte';
	import PhoneIcon from './icons/PhoneIcon.svelte';

	export let text: string;
	export let variant: 'email' | 'phone' | 'location';
</script>

<div class="flex antialiased items-center gap-2">
	{#if variant === 'email'}
		<EmailIcon />
	{:else if variant === 'phone'}
		<PhoneIcon />
	{:else if variant === 'location'}
		<LocationIcon />
	{/if}
	<p class="antialiased">{text}</p>
</div>

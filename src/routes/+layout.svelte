<script lang="ts">
	import '../app.postcss';
</script>

<svelte:head>
	<title>Jannis Karanikis</title>
	<meta
		name="description"
		content="CV/Resume Page For Jannis Karanikis Software Engineer, Frontend Developer, Test Specialist and Cyber Security Enthusiast."
	/>
</svelte:head>;
<div class="flex justify-center shadow">
	<div class="lg:my-8 lg:grid grid-cols-8 lg:h-screen lg:w-3/4">
		<slot />
	</div>
</div>

<script lang="ts">
	import Card from '$lib/components/Card.svelte';
	import Title from '$lib/components/Title.svelte';
	import UserIcon from '$lib/components/icons/UserIcon.svelte';
	import CaseIcon from '$lib/components/icons/CaseIcon.svelte';
	import Contact from '$lib/components/Contact.svelte';
	import Job from '$lib/components/Job.svelte';

	const jobList = [
		{
			title: 'Software Engineer | Software Engineer In Test',
			company: 'Avega',
			from: 'Oct 2021',
			to: 'Present',
			description: [
				'Test Automation Lead.',
				'Mentored juniors and conducted code reviews.',
				'Worked closely with other developers to improve quality of application code.',
				`Implemented security measures to protect company's data.`,
				'Focused on enchancing frontend performance and accesibility.'
			]
		},
		{
			title: 'Technical Tester',
			company: 'Nordicstation',
			from: 'Jan 2020',
			to: 'Oct 2021',
			description: [
				'Test Lead on multiple projects.',
				'Led development and planning of test automation.',
				'Assisted in development of backend and frontend code.'
			]
		}
	];
</script>

<div
	class="bg-surface-700 bg-opacity-50 p-5 h-full col-span-2 rounded-l-2xl flex flex-col gap-6 items-center"
>
	<enhanced:img
		src="/src/lib/assets/super-handsome-man.png"
		alt="Handsome and super cool guy"
		class="rounded-full shadow-lg w-48 h-auto mt-4"
	/>
	<div class="flex flex-col gap-2">
		<h3 class="h3">Jannis Karanikis</h3>
		<div class="flex flex-col">
			<Title>Software Engineer</Title>
			<Title>Test Specialist</Title>
			<Title>Cyber Security Enthusiast</Title>
		</div>
		<div class="flex flex-col gap-4 mt-8">
			<h3 class="h3">Contact</h3>
			<Contact text="Jannis.Karanikis@gmail.com" variant="email" />
			<Contact text="+46763075418" variant="phone" />
			<Contact text="Stockholm, Sweden" variant="location" />
		</div>
	</div>
</div>
<div class="col-span-4 bg-surface-700 bg-opacity-15">
	<Card>
		<div class="flex gap-1 items-center mb-5">
			<UserIcon />
			<h3 class="h3">About Me</h3>
		</div>
		<p class="font-sans font-light antialiased">
			I am a software engineer with expertise in TypeScript and strong knowledge of C# and Go. I
			specialize in test automation, frontend development, cybersecurity, and DevOps. With a solid
			background in testing, several years of professional and open-source programming experience,
			and a passion for continuous improvement.
		</p>
		<p class="font-sans font-light antialiased">
			I strive to create robust and secure systems while staying up to date with the latest industry
			trends.I am a software engineer with expertise in TypeScript and strong knowledge of C# and
			Go. I specialize in test automation, frontend development, cybersecurity, and DevOps.
		</p>
	</Card>
	<Card>
		<div class="flex gap-1 items-center mb-5">
			<CaseIcon />
			<h3 class="h3">Work Experience</h3>
		</div>
		{#each jobList as job}
			<Job {...job} />
		{/each}
	</Card>
</div>
<div class="bg-surface-700 bg-opacity-50 p-5 h-full col-span-2 rounded-r-2xl">
	<h1 class="text-2xl font-bold">Hello World</h1>
	<p class="text-gray-600">This is a sample page</p>
</div>

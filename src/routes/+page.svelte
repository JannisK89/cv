<script lang="ts">
	import Card from '$lib/components/Card.svelte';
	import Title from '$lib/components/Title.svelte';
	import UserIcon from '$lib/components/icons/UserIcon.svelte';
	import CaseIcon from '$lib/components/icons/CaseIcon.svelte';
	import Contact from '$lib/components/Contact.svelte';
	import Skill from '$lib/components/Skill.svelte';
	import Job from '$lib/components/Job.svelte';
	import EducationIcon from '$lib/components/icons/EducationIcon.svelte';
	import ComputerIcon from '$lib/components/icons/ComputerIcon.svelte';
	import Quote from '$lib/components/Quote.svelte';
	import { links, quotes, skills, jobList } from '$lib/data';
	import Section from '$lib/components/Section.svelte';
	import Link from '$lib/components/Link.svelte';
</script>

<div
	class="bg-surface-700 bg-opacity-50 p-5 xl:h-full col-span-2 xl:rounded-l-2xl flex flex-col xl:gap-6 items-center pb-16"
>
	<enhanced:img
		src="/src/lib/assets/super-handsome-man.png"
		alt="Handsome and super cool guy"
		class="rounded-full shadow-lg w-48 h-auto my-4 xl:my-0"
	/>
	<div class="flex flex-col gap-2">
		<h3 class="h3">Jannis Karanikis</h3>
		<div class="flex flex-col">
			<Title>Ethical Hacker | Security Tester</Title>
			<Title>Software Engineer</Title>
			<Title>Test Specialist</Title>
		</div>
		<Section>
			<h3 class="h3">Contact</h3>
			<Contact text="Jannis.Karanikis@gmail.com" variant="email" />
			<Contact text="+46763075418" variant="phone" />
			<Contact text="Stockholm, Sweden" variant="location" />
		</Section>
		<Section>
			<h3 class="h3">Links</h3>
			{#each links as link}
				<Link {...link} />
			{/each}
		</Section>
	</div>
</div>
<div class="col-span-4 bg-surface-700 bg-opacity-15">
	<Card>
		<div class="flex gap-1 items-center mb-5">
			<UserIcon />
			<h3 class="h3">About Me</h3>
		</div>
		<p class="font-sans font-light antialiased text-base">
    I am an IT security professional who bridges the critical gap between
    offensive security and software development. My primary focus is on
    proactively discovering and neutralizing threats in web and API ecosystems.
    Leveraging hands-on development experience with TypeScript (React/NextJS,
    Svelte/SvelteKit) and Go, I not only identify weaknesses through rigorous
    testing but also collaborate directly with engineering teams to implement
    effective, long-term security solutions. With a strong foundation in DevOps
    and cloud infrastructure, I champion a security-first mindset across the
    entire SDLC. I actively contribute to the security community as a speaker
    and writer, sharing insights on both secure development and vulnerability
    assessment.
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
	<Card>
		<div class="flex gap-1 items-center mb-5">
			<EducationIcon />
			<h3 class="h3">Education</h3>
		</div>
		<Job
			title="Quality Assurance And Testing in IT"
			company="Nackademin"
			from="2018"
			to="2020"
      gap={false}
			description={[
				'2 year vocational education.',
				'Test and test methodologies.',
				'Test automation',
				'Backend and Frontend development'
			]}
		/>
	</Card>
	<Card>
		<div class="flex gap-1 items-center mb-5">
			<ComputerIcon />
			<h3 class="h3">Skills</h3>
		</div>
		<ul class="flex flex-wrap gap-2">
			{#each skills as skill}
				<Skill title={skill} />
			{/each}
		</ul></Card
	>
</div>
<div class="bg-surface-700 bg-opacity-50 p-5 xl:h-full col-span-2 rounded-r-2xl">
	<h3 class="h3 mb-6">Testimonials</h3>
	<div class="flex flex-col gap-8">
		{#each quotes as quote}
			<Quote {...quote} />
		{/each}
	</div>
</div>

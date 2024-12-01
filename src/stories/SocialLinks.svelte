<script lang="ts">
	interface SocialLink {
		href: string;
		icon: string;
		iconUrl: string;
	}

	export let variant: 'horizontal' | 'vertical' = 'vertical';
	export let socialLinks: SocialLink[] = [];
</script>

<div
	class="flex items-center gap-3"
	class:flex-row={variant === 'horizontal'}
	class:flex-col={variant === 'vertical'}
>
	{#each socialLinks as { href, icon, iconUrl }}
		<a
			{href}
			target="_blank"
			rel="noopener noreferrer"
			class="rounded-lg bg-secondary p-2 transition-colors duration-200 hover:bg-secondary/80"
		>
			<img src={iconUrl} alt={icon} class="h-5 w-5" />
		</a>
	{/each}
</div>

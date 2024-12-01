<script module>
	import { defineMeta } from '@storybook/addon-svelte-csf';
	import SocialLinks from './SocialLinks.svelte';

	const { Story } = defineMeta({
		title: 'Components/SocialLinks',
		component: SocialLinks,
		tags: ['autodocs'],
		parameters: {
			layout: 'centered'
		},
		argTypes: {
			variant: {
				control: 'select',
				options: ['horizontal', 'vertical'],
				description: 'Layout direction of social media links'
			},
			socialLinks: {
				control: 'object',
				description: 'Array of social media links',
				defaultValue: [
					{ href: 'https://twitter.com', icon: 'twitter', iconUrl: '/icons/twitter.svg' },
					{ href: 'https://github.com', icon: 'github', iconUrl: '/icons/github.svg' },
					{ href: 'https://linkedin.com', icon: 'linkedin', iconUrl: '/icons/linkedin.svg' }
				]
			}
		}
	});
</script>

<Story
	name="Vertical"
	args={{
		variant: 'vertical',
		socialLinks: [
			{ href: 'https://twitter.com', icon: 'twitter', iconUrl: '/icons/twitter.svg' },
			{ href: 'https://github.com', icon: 'github', iconUrl: '/icons/github.svg' },
			{ href: 'https://linkedin.com', icon: 'linkedin', iconUrl: '/icons/linkedin.svg' }
		]
	}}
/>

<Story
	name="Horizontal"
	args={{
		variant: 'horizontal',
		socialLinks: [
			{ href: 'https://twitter.com', icon: 'twitter', iconUrl: '/icons/twitter.svg' },
			{ href: 'https://github.com', icon: 'github', iconUrl: '/icons/github.svg' },
			{ href: 'https://linkedin.com', icon: 'linkedin', iconUrl: '/icons/linkedin.svg' }
		]
	}}
/>

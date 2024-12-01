<script lang="ts">
	import { Map, Calendar, Link, Play, Share2 } from 'lucide-svelte';
	import { Button } from '$lib/components/ui/button';

	let stream = true;
</script>

<div class="relative p-4">
	<div class="h-40 w-full rounded-xl bg-neutral-200"></div>
	<div class="mt-4 flex items-center gap-2">
		<div class="h-12 w-12 rounded-xl bg-neutral-200"></div>
		<div class="h-12 w-12 rounded-xl bg-neutral-200"></div>
		<div class="h-12 w-12 rounded-xl bg-neutral-200"></div>
		<div class="h-12 w-12 rounded-xl bg-neutral-200"></div>
		<div
			class="absolute bottom-2 right-2 ml-auto box-content h-32 w-32 rounded-full border-[12px] border-white bg-neutral-200"
		></div>
	</div>
</div>

<div class="flex flex-col gap-3 p-4">
	<div class="flex w-full items-center justify-between">
		<div class="flex items-center gap-3">
			<div class="space-y-1">
				<h1 class="text-lg font-semibold tracking-tight">AMBRA Vol. 1</h1>
			</div>
		</div>

		<Button variant="link" class="rounded-full outline outline-neutral-200">
			<Share2 class="h-4 w-4" />
		</Button>
	</div>
	<div class="relative max-h-full min-h-48 w-full rounded-xl bg-neutral-200">
		<div class="absolute bottom-2 right-4 text-neutral-700 underline">Explore Catalogue</div>
	</div>
</div>

{#if stream}
	<div class="flex flex-col gap-3 p-4">
		<div class="flex w-full items-center justify-between">
			<div class="flex items-center gap-3">
				<Button variant="link" class="rounded-full outline outline-neutral-200">
					<Play class="h-4 w-4" />
				</Button>
				<div class="space-y-1">
					<h1 class="text-lg font-semibold tracking-tight">Live Sale</h1>
				</div>
			</div>

			<Button variant="link" class="rounded-full outline outline-neutral-200">
				<Share2 class="h-4 w-4" />
			</Button>
		</div>
		<div class="flex gap-4">
			<div class="relative max-h-full w-full overflow-clip rounded-xl bg-neutral-200">
				<div class="absolute top-0 flex w-full items-center justify-between">
					<h1
						class="rounded-br-xl bg-red-500 px-4 py-1 text-sm font-semibold tracking-tight text-neutral-50"
					>
						Promo 12.12
					</h1>
				</div>
			</div>
			<div class="flex flex-col items-center gap-2">
				<div class="h-12 w-12 rounded-xl bg-neutral-200"></div>
				<div class="h-12 w-12 rounded-xl bg-neutral-200"></div>
				<div class="h-12 w-12 rounded-xl bg-neutral-200"></div>
				<div class="h-12 w-12 rounded-xl bg-neutral-200"></div>
			</div>
		</div>
	</div>
{/if}

<div class="flex flex-col gap-3 p-4">
	<div class="flex w-full items-center justify-between">
		<div class="flex items-center gap-3">
			<div class="space-y-1">
				<h1 class="text-lg font-semibold tracking-tight">Ayo ketemuan!</h1>
			</div>
		</div>

		<div class="flex gap-2">
			<Button variant="link" class="rounded-full outline outline-neutral-200">
				<Calendar class="h-4 w-4" />
			</Button>
			<Button variant="link" class="rounded-full outline outline-neutral-200">
				<Map class="h-4 w-4" />
			</Button>
		</div>
	</div>
	<div class="relative max-h-full min-h-48 w-full rounded-xl bg-neutral-200"></div>
</div>

<div class="flex flex-col gap-3 p-4">
	<div class="flex w-full items-center justify-between">
		<div class="flex items-center gap-3">
			<div class="space-y-1">
				<h1 class="text-lg font-semibold tracking-tight">Link Lainnya</h1>
			</div>
		</div>
	</div>
	<div class="flex items-center justify-between rounded-xl bg-neutral-200 px-4 py-2">
		<h2>Link 1</h2>
		<Button variant="link" class="rounded-full outline outline-neutral-200">
			<Link class="h-4 w-4" />
		</Button>
	</div>
	<div class="flex items-center justify-between rounded-xl bg-neutral-200 px-4 py-2">
		<h2>Link 2</h2>
		<Button variant="link" class="rounded-full outline outline-neutral-200">
			<Link class="h-4 w-4" />
		</Button>
	</div>
	<div class="flex items-center justify-between rounded-xl bg-neutral-200 px-4 py-2">
		<h2>Link 3</h2>
		<Button variant="link" class="rounded-full outline outline-neutral-200">
			<Link class="h-4 w-4" />
		</Button>
	</div>
</div>

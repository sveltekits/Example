<script lang="ts">
	import type { PageServerData } from './$types';
	export let data: PageServerData;
</script>

<svelte:head>
	<title>즐거운 쇼핑</title>
</svelte:head>

<h1>상품 목록</h1>
{#each data.products as product}
	<h2>목록</h2>
{/each}

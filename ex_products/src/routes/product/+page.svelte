<script lang="ts">
	import type { PageServerData } from './$types';
	export let data: PageServerData;
</script>

<svelte:head>
	<title>즐거운 쇼핑</title>
</svelte:head>

<h1>상품 목록</h1>
<!-- product
	"id": 1,
    "title": "iPhone 9",
    "description": "An apple mobile which is nothing like apple",
    "price": 549,
    "discountPercentage": 12.96,
    "rating": 4.69,
    "stock": 94,
    "brand": "Apple",
    "category": "smartphones",
    "thumbnail": "https://cdn.dummyjson.com/product-images/1/thumbnail.jpg",
    "images": [
        "https://cdn.dummyjson.com/product-images/1/1.jpg",
        "https://cdn.dummyjson.com/product-images/1/2.jpg",
        "https://cdn.dummyjson.com/product-images/1/3.jpg",
        "https://cdn.dummyjson.com/product-images/1/4.jpg",
        "https://cdn.dummyjson.com/product-images/1/thumbnail.jpg"
    ]
-->
{#each data.products as product}
	<a href={`/product/${product.id}`}>
		<h2>{product.title} [{product.brand}]</h2>
	</a>
	<h3>category : {product.category}</h3>
	<img src={product.thumbnail} alt="" />
	<hr />
{/each}

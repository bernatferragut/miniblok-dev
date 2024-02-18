<script>
	import * as config from '$lib/config'
	export let data
</script>

<!-- <pre>
	{JSON.stringify(data, null,2)}
</pre> -->

<svelte:head>
	<title>{config.title}</title>
</svelte:head>

<!-- Posts -->
<section>
	<ul class="posts">
		{#each data.posts as post}
			<li class="post">
				<a href={post.slug} class="title">{post.title}</a>
				<!-- svelte-ignore a11y-missing-attribute -->
				<img src={post.preview} width="300" height="100">
				<p class="description">{post.description}</p>
				<p class="date">{post.date}</p>
			</li>
		{/each}
	</ul>
</section>

<style>
	.posts {
		display: grid;
		gap: var(--size-7);
	}

	.post {
		max-inline-size: var(--size-content-3);
		/* font-size: var(--font-size-fluid-0); */
	}

	.post:not(:last-child) {
		border-bottom: 1px solid var(--border);
		padding-bottom: var(--size-7);
	}

	.title {
		font-size: var(--font-size-fluid-1);
		text-transform: capitalize;
	}

	.date {
		/* font-family: var(--font-mono); */
		font-size: var(--font-size-fluid-0);
		color: var(--text-2);
	}

	.description {
		font-family: var(--font-mono);
		margin-top: var(--size-3);
		font-size: var(--font-size-fluid-0);
	}
</style>

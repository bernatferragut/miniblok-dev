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
<section >
	<ul class="posts">
		{#each data.posts as post}
		<div >
			<li class="post">
				<a href={post.slug} class="title">{post.title}</a>
				<!-- svelte-ignore a11y-missing-attribute -->
				<img src={post.preview} width=100% height="100%">
				<p class="description">{post.description} | <span class="date"> {post.date}</span></p>
			</li>
		</div>
		{/each}

	</ul>
</section>


<style>

	/* section {
		font-family: var(--font-mono);
	} */

	.cards {
  		display: grid;
  		grid-template-columns: repeat(3, 1fr); /* you can change 1fr to whatever you want, 200px for example*/
  		gap: 2rem;
	}

	.card {
  		border: 1px solid red;
  		min-height: 200px;
	}
	.posts {
		display: grid;
		gap: var(--size-7);
		
	}

	.post {
		max-inline-size: var(--size-content-3);
		font-size: var(--font-size-fluid-0);
		/* margin: 0 auto; */
		
	}

	.post:not(:last-child) {
		border-bottom: 1px solid var(--border);
		padding-bottom: var(--size-5);
	}

	.title {
		font-size: var(--size-3);
		text-transform: capitalize;
	}

	a:visited {
		color: hex(#ffc078);
		text-decoration-color: hex(#ffc078);
	}

	.date {
		font-size: var(--font-size-fluid-0);
		color: var(--text-2);
	}

	.description {
		margin-top: var(--size-3);
		font-size: var(--font-size-fluid-0);
	}
</style>

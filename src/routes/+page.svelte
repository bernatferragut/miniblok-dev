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

	section {
		font-family: 'Silkscreen', system-ui;
        color: #FCCC8E;
        padding-block: 10px ;
		/* background-color: black; */
	}

	.posts {
		display: grid;
		gap: 2rem;
		
	}

	.post {
		max-inline-size: 100%;
		font-size: 1rem;
		list-style-type: none;
		margin: 0 auto;
		
	}

	.post:not(:last-child) {
		border-bottom: 1px solid;
		padding-bottom: 10px;
	}

	.title {
		color: #ffc078;
		font-size: 1rem;
		text-transform: capitalize;
	}

	a {
		text-decoration-color: currentcolor;
	}
	
	a:visited {
		color: hex(#ffc078);
		text-decoration-color: hex(#ffc078);
	}

	.date {
		font-size: 1rem;
		color: #ffc078;
	}

	.description {
		margin-top: 1rem;
		font-size: 1rem;
	}
</style>

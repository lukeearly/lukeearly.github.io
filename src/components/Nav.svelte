<script>
	export let segment;
</script>

<style>
	nav {
		border-bottom: 1px solid rgba(51, 51, 51, 0.2);
		background-color: #f8f8f8;
		font-weight: 200;
		font-family: 'Courier New', Courier, monospace;
		padding: 0 1em;
		flex: 0 1 auto;
	}

	ul {
		margin: 0;
		padding: 0;
	}

	/* clearfix */
	ul::after {
		content: '';
		display: block;
		clear: both;
	}

	li { display: block; }
	li.left { float: left; }
	li.right { float: right; }

	[aria-current] {
		position: relative;
		display: inline-block;
	}

	[aria-current]::after {
		position: absolute;
		content: '';
		width: calc(100% - 2em);
		height: 2px;
		background-color: rgb(214, 20, 20);
		display: block;
		bottom: -1px;
	}

	a {
		text-decoration: none;
		padding: 1em 1em;
		display: block;
	}
</style>

<nav>
	<ul>
		<li class='left'><a aria-current="{segment === undefined ? 'page' : undefined}" href=".">home</a></li>
		<li class='left'><a aria-current="{segment === 'portfolio' ? 'page' : undefined}" href="portfolio">portfolio</a></li>

		<!-- for the blog link, we're using rel=prefetch so that Sapper prefetches
		     the blog data when we hover over the link or tap it on a touchscreen -->
		<!-- <li class='left'><a rel=prefetch aria-current="{segment === 'blog' ? 'page' : undefined}" href="blog">blog</a></li> -->

		<li class='right'><a href="https://github.com/lukeearly">github</a></li>
		<!-- <li class='right'><a href="https://gitlab.com/lukeearly">gitlab</a></li> -->
		<!-- <li class='right'><a href="https://hydros.team">hydros</a></li> -->
	</ul>
</nav>

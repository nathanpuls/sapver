<script>
	export let segment;
</script>

<style>
	nav {
		border-bottom: 1px solid #ccc;
		font-weight: 300;
		padding: 0 1em;
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

	li {
		display: block;
		float: left;
	}

	.selected {
		position: relative;
		display: inline-block;
	}

	.selected::after {
		position: absolute;
		content: '';
		width: calc(100% - 1em);
		height: 2px;
		background-color: #008acb;
		display: block;
		bottom: -1px;
	}

	a {
		text-decoration: none;
		padding: 1em 0.5em;
		display: block;
	}
</style>

<nav>
	<ul>
		<li><a aria-current="{segment === undefined ? 'page' : undefined}" href=".">Demos</a></li>
		<li><a aria-current="{segment === 'projects' ? 'page' : undefined}" href="projects">Projects</a></li>
		<li><a aria-current="{segment === 'studio' ? 'page' : undefined}" href="studio">Studio</a></li>
		<li><a aria-current="{segment === 'clients' ? 'page' : undefined}" href="clients">Clients</a></li>
		<li><a aria-current="{segment === 'reviews' ? 'page' : undefined}" href="reviews">Reviews</a></li>
		<li><a aria-current="{segment === 'about' ? 'page' : undefined}" href="about">About</a></li>
		<li><a aria-current="{segment === 'podcast' ? 'podcast' : undefined}" href="podcast">Podcast</a></li>
		<li><a aria-current="{segment === 'contact' ? 'page' : undefined}" href="contact">Get in touch</a></li>
	</ul>
</nav>
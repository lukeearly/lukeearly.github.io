<script>
	import dag from "images/dag.png";
	import hydros from "images/hydros.png";
	import Aside from "../components/Aside.svelte";
</script>

<style>
	ul {
		/* display: grid;
		grid-template-columns: auto auto; */
		margin: 0;
		padding: 0;
	}

	li {
		display: block;
		outline: 1px solid rgba(51, 51, 51, 0.2);
		outline-offset: .5em;
		margin: 1.5em 0;
		padding: .5em 0;
	}

	img {
		width: 100%;
		margin: auto;
	}
</style>

<svelte:head>
	<title>portfolio | luke early</title>
</svelte:head>

<h1>Portfolio</h1>

<ul>
	<li><a href="https://github.com/whhsftc/switchboard">switchboard</a> library for FTC robotics to <Aside id="dag" side="left"><span slot="summary">schedule software and hardware commands,</span>Command scheduler: <img src={dag} alt="Switchboard command graph"></Aside> used in our team's award-winning 2021-2022 season as lead programmer</li>
	<li><a href="https://github.com/lukeearly/gabp">GaBP</a> library including linear algebra and statistics to experiment with Gaussian belief propagation</li>
	<li><a href="https://github.com/lukeearly/aspera">aspera</a> kernel, C library, and initial RAM filesystem (currently shelved in favor of a rewrite in Rust)</li>
	<li><a href="https://github.com/lukeearly/swarm">swarm</a>, library of Nix utils and modules for configuring a group of connected NixOS machines</li>
	<li><a href="https://github.com/lukeearly/psil">psil</a> and <a href="https://github.com/lukeearly/pherrite">pherrite</a>, two simple language designs</li>
	<li><a href="https://github.com/lukeearly/chords">chords</a>, a command-line app to view user-generated iReal Pro charts without buying a license to the app</li>
	<li>Competing with <Aside id="hydros" side="right"><span slot="summary">hydroelectricities</span><a href="https://ctftime.org/team/157985">CTFtime</a><img src={hydros} alt="hydroelectricities"></Aside>, a small hacking collaborative and CTF team</li>
	<li>Maintainer of hydroelectricities' infrastructure using swarm</li>
	<li><a href="https://github.com/lukeearly/lukeearly.github.io">this website</a>, written using Svelte and Sapper to create a modern static blog with minimal JavaScript running client-side</li>
	<!-- <li><a href="blog/:projects">And more...</a></li> -->
</ul>
<script>
	import Aside from "../components/Aside.svelte";
</script>

<style>
	h1 {
		font-size: 2em;
	}

	@media (min-width: 400px) {
		h1 {
			font-size: 3em;
		}
	}
</style>

<svelte:head>
	<title>about | luke early</title>
</svelte:head>

<h1>Luke Early</h1>

<p>I'm a student, engineer, and musician with interest in cybersecurity and robotics. Check out my <a href="https://github.com/lukeearly">open source work</a> and a selected <a href="portfolio">portfolio</a> of some projects I'm proud of!</p>

<h2>Skills</h2>
<ul>
	<li>C, Rust, Kotlin, Python, and other languages</li>
	<li>NixOS multi-machine configuration and deployment</li>
	<li>Systems programming</li>
	<li>Reverse engineering</li>
	<li>Control theory</li>
	<li>Web development</li>
</ul>

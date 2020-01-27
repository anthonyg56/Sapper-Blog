<script>
	import Home from '../components/Home/Home.svelte'
	import { onMount } from 'svelte'

  	onMount(() => {
		if (window.netlifyIdentity) {
			window.netlifyIdentity.on("init", user => {
				if (!user) {
					window.netlifyIdentity.on("login", () => {
						document.location.href = "/admin/"
					})
				}
			})
		}
  	})
</script>

<svelte:head>
	<title>A Creatives Blog</title>
	<script src="https://identity.netlify.com/v1/netlify-identity-widget.js"></script>
</svelte:head>

<Home />
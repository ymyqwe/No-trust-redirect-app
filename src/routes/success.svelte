<svelte:head>
	<title>Success</title>
</svelte:head>

<h1>Successfully Validated</h1>

<p>You are good to go with you application. You can close this tab now.</p>


<script>

import { onMount } from 'svelte';
import { stores } from "@sapper/app";

const { page } = stores();
console.log($page.query);

onMount(() => {
	setTimeout(() => {
		window.close();
	}, 1000);
});

</script>
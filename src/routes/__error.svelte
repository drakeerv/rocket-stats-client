<script context="module">
	export function load({ error, status }) {
		return {
			props: {
				status: status.toString(),
				message: error.message
			}
		};
	}
</script>

<script lang="ts">
	export let status: string;
	export let message: string;
</script>

<svelte:head>
	<title>RocketStats - Error {status}</title>
</svelte:head>

<h1 class="font-bold text-center">{status}</h1>
<h2 class="text-center">{message}</h2>
<p class="text-center">Oops! You ran into an error! Try going <a sveltekit:prefetch href="/">home?</a></p>

<style>
    h1 {
        font-size: 100px;
    }

    h2 {
        font-size: 25px;
    }
</style>
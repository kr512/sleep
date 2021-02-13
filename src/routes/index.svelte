<script>
import _sleep from "@ilsubyeega/sleep-js";
const sleep = new _sleep();
</script>

<style>

</style>

<svelte:head>
	<title>Home (Sleep)</title>
</svelte:head>

{sleep.getSleepTime(0, 6)}
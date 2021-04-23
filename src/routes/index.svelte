<script>
import _sleepjs from "@ilsubyeega/sleep-js";
const sleep = new _sleepjs();
</script>

<style>

</style>

<svelte:head>
	<title>Home (Sleep)</title>
</svelte:head>

{sleep.getSleepTime(0, 6)}
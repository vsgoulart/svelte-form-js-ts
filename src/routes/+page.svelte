<script>
	import { onMount } from 'svelte';
	import schema from './schema.json';
	import '@bpmn-io/form-js/dist/assets/form-js.css';

	onMount(async () => {
		const { Form } = await import('@bpmn-io/form-js');
		const form = new Form({
			container: '#container'
		});

		form.importSchema(schema);
	});
</script>

<main>
	<div id="container" />
</main>

<style>
	main {
		width: 100vw;
		height: 100vh;
	}
	#container {
		width: 100%;
		height: 100%;
	}
</style>

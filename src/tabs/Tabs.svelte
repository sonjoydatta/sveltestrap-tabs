<script lang="ts">
	import { onMount } from 'svelte';

	export let defaultId: string;

	onMount(() => {
		let target = document.querySelector(`#${defaultId}`);
		if (target) {
			let headParent = target.querySelectorAll('.nav-tabs');
			let contentParent = target.querySelectorAll('.tab-content');

			if (headParent && contentParent) {
				headParent[0].querySelector('li').querySelector('a').classList.add('active');
				contentParent[0].querySelector('.tab-pane').classList.add('show', 'active');
			}
		}
	});
</script>

<div id={defaultId}>
	<slot />
</div>

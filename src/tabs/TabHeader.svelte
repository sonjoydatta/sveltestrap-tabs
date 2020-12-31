<script lang="ts">
	export let id: string = 'svelte';
</script>

<ul class="nav nav-tabs" {id} role="tablist">
	<slot />
</ul>

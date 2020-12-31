<script lang="ts">
	export let id!: string;
</script>

<div class="tab-pane fade" {id} role="tabpanel" aria-labelledby={`${id}-tab`}>
	<slot />
</div>

<script lang="ts">
	import { onMount } from "svelte";

    let text = "";
    
    onMount(() => {
        loadText();
    });

    async function loadText() {
        const resp = await fetch("test.md");
        text = await resp.text();
    }
</script>

<h1>Click a link!</h1>

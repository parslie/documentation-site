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

<h1>Welcome to SvelteKit</h1>
<p>{text}</p>

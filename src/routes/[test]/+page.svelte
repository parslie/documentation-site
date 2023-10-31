<script lang="ts">
    import { page } from "$app/stores";
    const test: string = $page.params.test;
</script>

<p>{test}</p>
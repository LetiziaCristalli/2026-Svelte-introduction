<script>
    import ClickCounter from "$lib/components/ClickCounter.svelte"
    import CanvasSquare from "$lib/components/CanvasSquare.svelte"

    let count= $state(5);
    let double = $derived(count * 2);
</script>

<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://svelte.dev/docs/kit">svelte.dev/docs/kit</a> to read the documentation</p>

<ClickCounter bind:initialCount={count} />

{#if count > 10 && count < 20}
    <p>count from parent is {count}</p>
{/if}

<CanvasSquare />

<style>
    h1  {
        color: deepskyblue;
    }
</style>
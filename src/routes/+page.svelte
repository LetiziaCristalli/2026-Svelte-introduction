<script>
    import ClickCounter from "$lib/components/ClickCounter.svelte"

    let count= $state(5);
    let double = $derived(count * 2);
</script>

<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://svelte.dev/docs/kit">svelte.dev/docs/kit</a> to read the documentation</p>

<ClickCounter bind:initialCount={count} />
<p>count from parent is {count}</p>

<style>
    h1  {
        color: deepskyblue;
    }
</style>


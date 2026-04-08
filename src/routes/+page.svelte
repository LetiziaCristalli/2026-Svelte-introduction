<script>
    import {website} from "$lib/state.svelte"

    import ClickCounter from "$lib/components/ClickCounter.svelte"
    import CanvasSquare from "$lib/components/CanvasSquare.svelte"
    import Todolist from "$lib/components/todolist.svelte";
    import TitleEditor from "$lib/components/TitleEditor.svelte";

    let count= $state(5);
    let double = $derived(count * 2);
</script>

<h1>{website.title}</h1>
<p>Visit <a href="https://svelte.dev/docs/kit">svelte.dev/docs/kit</a> to read the documentation</p>
<TitleEditor />

<ClickCounter bind:initialCount={count} />

{#if count > 10 && count < 20}
    <p>count from parent is {count}</p>
{:else if count > 30 } 
    <p>that's a lot of click!</p>
{:else}
    <p>count is not in range</p>
{/if}

<CanvasSquare />
<Todolist />

<style>
    h1  {
        color: deepskyblue;
    }
</style>
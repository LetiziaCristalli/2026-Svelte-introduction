<script>
    let todos = $state([
        {title: "Assigmnment 1", done: false},
        {title: "Assigmnment 2", done: false},
        {title: "Assigmnment 3", done: false},
    ]);
</script>
<h3>My Todos</h3>
<ul>
    {#each todos as todo}
    <li>
        <input type="checkbox" bind:checked={todo.done}>
        {todo.title}</li>
    {/each}
</ul>
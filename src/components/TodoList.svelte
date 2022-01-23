<script>
    import { todos } from '../store/TodoStore.ts'
</script>

<ul>
    {#each $todos as todo}
        <li>{todo}</li>
    {/each}
</ul>

<style>
    ul {
        display: flex;
        flex-direction: column;
        justify-content: center;
        max-width: 500px;
        margin: auto;
    }
    li {
        text-align: start;
    }
</style>
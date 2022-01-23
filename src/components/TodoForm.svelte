<script>
    import { todos } from '../store/TodoStore.ts'

    let todo = ''

    const handleTodo = e => {
        e.preventDefault();
        todos.update(todos => {
            return [todo, ...todos]
        })

        todo = ''
    }
</script>

<form>
    <label>
        Todo Item
        <input type="text" bind:value={todo}>
        <button on:click={handleTodo}>Add item</button>
    </label>
</form>
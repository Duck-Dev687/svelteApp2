<script>
    let todo = '';
    import {addTodo} from "../stores/todoStore.js"
    const handleSubmit = () =>{
        addTodo(todo)
        todo=''
        console.log("submitting!")
    }
</script>

<form on:submit|preventDefault={handleSubmit} class="my-6">
<div class="flex flex-col text-sm mb-2">
    <label class="font-bold mb-2 text-gray-800" for="todo">Todo</label>
    <input class="appearance-none shadow-sm border border-gray-200 p-2 focus:outline-none focus:border-gray-500 rounded-lg" type="text" name="todo" bind:value={todo} placeholder="Watcha gotta do?">
</div>

<button type="submit" class="w-full shadow-sm rounded bg-blue-500 hover:bg-blue-600 text-white py-2 px-4">Submit</button>
</form>
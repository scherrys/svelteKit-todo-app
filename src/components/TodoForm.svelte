<script>
	let todo = '';
	import { addTodo } from '../stores/todoStore';

	const handleSubmit = () => {
		addTodo(todo);
		console.log(todo);
		todo = '';
	};
</script>

<form class="my-6" on:submit|preventDefault={handleSubmit}>
	<div class="flex flex-col text-sm mb-2">
		<label class="font-bold mb-2 text-gray-800" for="todo">Todo</label>
		<input
			type="text"
			name="todo"
			placeholder="Watcha gotta do?"
			class="apperance-none shadow-sm border border-gray-200 p-2 focus:outline-none focus:border-gray-500 rounded-lg"
			bind:value={todo}
		/>
	</div>
	<button
		class="w-full shadow-sm bg-blue-500 rounded hover:bg-blue-600 text-white py-2 px-4"
		type="submit">Submit</button
	>
</form>

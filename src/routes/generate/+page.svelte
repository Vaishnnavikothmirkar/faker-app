
<script>
  import { Heading, Input, NumberInput,Span,Label, Select } from 'flowbite-svelte';
  import { Checkbox } from 'flowbite-svelte';
  let FormatTypes = [
		{ value: 'html', name: 'HTML' },
		{ value: 'csv', name: 'CSV' },
		{ value: 'json', name: 'JSON' }
	];
  let FormatType= "csv";
   let value = "5";
   import {  ButtonGroup} from 'flowbite-svelte';
   export let data;
  function handleSubmit(event) {


   console.log(data); }
</script>
 
 <Heading tag="h3" class="mb-2 p-3 py-8 text-center">Generate Data <Span highlight><br></Span> <Span gradient></Span></Heading>
 <div>
   <form id="inputForm" on:submit|preventDefault={handleSubmit}>
   <div class="py-8 px-4 mx-auto max-w-screen-xl items-center text-left grid gap-6 xs:grid-cols-1 sm:grid-cols-3 grid-cols-2 space-y-0 ">
  <div>
    <p class="mb-4 font-semibold text-gray-900 dark:text-white">Person</p>
    <ul class="w-48 bg-white rounded-lg border border-gray-200 dark:bg-gray-800 dark:border-gray-600 divide-y divide-gray-200 dark:divide-gray-600">
      <li><Checkbox name="fields" value="full_name" id="full_name" class="p-1.5">Full Name</Checkbox></li>
      <li><Checkbox name="fields" value="first_name" id="first_name" class="p-1.5">First Name</Checkbox></li>
      <li><Checkbox name="fields" value="middle_name" id="middle_name" class="p-1.5">Middle Name</Checkbox></li>
      <li><Checkbox name="fields" value="last_name" id="last_name" class="p-1.5">Last Name</Checkbox></li>
      <li><Checkbox name="fields" value="gender" id="gender" class="p-1.5">Gender</Checkbox></li>
      <li><Checkbox name="fields" value="phone_number" id="phone_number" class="p-1.5">Phone Number</Checkbox></li>
      <li><Checkbox name="fields" value="zodiac_sign" id="zodiac_sign" class="p-1.5">Zodiac Sign</Checkbox></li>
    </ul> 
 </div>
 <div>
    <p class="mb-4 font-semibold text-gray-900 dark:text-white">Finance</p>
    <ul class="w-48 bg-white rounded-lg border border-gray-200 dark:bg-gray-800 dark:border-gray-600 divide-y divide-gray-200 dark:divide-gray-600">
      <li><Checkbox name="fields" value="salary" id="salary" class="p-1.5">Salary</Checkbox></li>
      <li><Checkbox name="fields" value="insurance" id="insurance" class="p-1.5">Insurance</Checkbox></li>
      <li><Checkbox name="fields" value="taxes" id="taxes" class="p-1.5">Taxes</Checkbox></li>
      <li><Checkbox name="salary" value="salary" id="taxes" class="p-1.5">Savings</Checkbox></li>
    </ul>
 </div>
<div>
   <p class="mb-4 font-semibold text-gray-900 dark:text-white">Commerce</p>
    <ul class="w-48 bg-white rounded-lg border border-gray-200 dark:bg-gray-800 dark:border-gray-600 divide-y divide-gray-200 dark:divide-gray-600">
    <li><Checkbox name="fields" value="department" id="department" class="p-1.5">Department</Checkbox></li>
    <li><Checkbox name="fields" value="price" id="price" class="p-1.5">Price</Checkbox></li>
    <li><Checkbox name="fields" value="product" id="product" class="p-1.5">Product</Checkbox></li>
    <li><Checkbox name="fields" value="isbn" id="isbn" class="p-1.5">isbn</Checkbox></li>
    </ul>
  </div>
  <div>
    <p class="mb-4 font-semibold text-gray-900 dark:text-white">Vehicle</p>
     <ul class="w-48 bg-white rounded-lg border border-gray-200 dark:bg-gray-800 dark:border-gray-600 divide-y divide-gray-200 dark:divide-gray-600">
     <li><Checkbox name="fields" value="type" id="type" class="p-1.5">Type</Checkbox></li>
     <li><Checkbox name="fields" value="color" id="color" class="p-1.5">Color</Checkbox></li>
     <li><Checkbox name="fields" value="manufacturer" id="manufacturer" class="p-1.5">Manufacturer</Checkbox></li>
     <li><Checkbox name="fields" value="model" id="model" class="p-1.5">Model</Checkbox></li>
     <li><Checkbox name="fields" value="fuel" id="fuel" class="p-1.5">Fuel</Checkbox></li>
     </ul>
 </div> 
 <div>
    <p class="mb-4 font-semibold text-gray-900 dark:text-white">Institution</p>
     <ul class="w-48 bg-white rounded-lg border border-gray-200 dark:bg-gray-800 dark:border-gray-600 divide-y divide-gray-200 dark:divide-gray-600">
     <li><Checkbox name="fields" value="fees" id="fees" class="p-1.5">Fees</Checkbox></li>
     <li><Checkbox name="fields" value="campus" id="campus" class="p-1.5">Campus</Checkbox></li>
     <li><Checkbox name="fields" value="location" id="location" class="p-1.5">Location</Checkbox></li>
     <li><Checkbox name="fields" value="fields" id="fields" class="p-1.5">Fields</Checkbox></li>
     </ul>
 </div>
 <div>
  <p class="mb-4 font-semibold text-gray-900 dark:text-white">Animals</p>
   <ul class="w-48 bg-white rounded-lg border border-gray-200 dark:bg-gray-800 dark:border-gray-600 divide-y divide-gray-200 dark:divide-gray-600">
   <li><Checkbox name="fields" value="cat" id="cat" class="p-1.5">Cat</Checkbox></li>
   <li><Checkbox name="fields" value="dog" id="dog" class="p-1.5">Dog</Checkbox></li>
   <li><Checkbox name="fields" value="fish" id="fish" class="p-1.5">Fish</Checkbox></li>
   <li><Checkbox name="fields" value="snake" id="snake" class="p-1.5">Snake</Checkbox></li>
   <li><Checkbox name="fields" value="horse" id="horse" class="p-1.5">Horse</Checkbox></li>
   </ul>
</div>
 <br>
 <br>
 <div class="mb-6"> 
  <Label class="block mb-2">
    <span>Count of Data</span>
    <NumberInput bind:value />
  </Label>
  <br>
  <div>
    <ButtonGroup class="w-full">
      <div>
      <Label>Select a Format
        <Select items={FormatTypes} bind:value={FormatType} /> <!-- on:change={handleSubmit(event)  -->
      </Label>
      </div>
      <br> <br>
      <div>
        <button class="" type="submit">
        Submit
      </button></div>
    </ButtonGroup>
</div>
</div>
</div>
</form>
 <br>
 <div>
  <textarea value={" hi "} readonly class="custom-scrollbar focus:outline-0 focus:shadow-none block p-2.5 bg-transparent resize-none w-full h-full text-sm text-gray-900 border-0"/>
 </div>
 <br>
</div>

<!-- <script>
	let todos = [
		{ done: false, text: 'finish Svelte tutorial' },
		{ done: false, text: 'build an app' },
		{ done: false, text: 'world domination' }
	];

	function add() {
		todos = todos.concat({ done: false, text: '' });
	}

	function clear() {
		todos = todos.filter((t) => !t.done);
	}

	$: remaining = todos.filter((t) => !t.done).length;
</script>

<h1>Todos</h1>

{#each todos as todo}
	<div>
		<input type="checkbox" bind:checked={todo.done} />

		<input placeholder="What needs to be done?" bind:value={todo.text} disabled={todo.done} />
	</div>
{/each}

<p>{remaining} remaining</p>

<button on:click={add}> Add new </button>

<button on:click={clear}> Clear completed </button>

-->

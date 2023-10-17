<script>
	import { Heading, Input, NumberInput, Span, Label, Select } from 'flowbite-svelte';
	import { Checkbox } from 'flowbite-svelte';
	import { faker } from '@faker-js/faker';
	export let testData = [];
	let FormatTypes = [
		{ value: 'html', name: 'HTML' },
		{ value: 'csv', name: 'CSV' },
		{ value: 'json', name: 'JSON' }
	];
	let FormatType = 'csv';
	let DataCount = '10';
	let form = {
		person: {
			fullName: false,
			firstName: false,
			middleName: false,
			lastName: false,
			gender: false,
			phoneNumber: false,
			zodiacSign: false
		},
		finance: {
			salary: false,
			insurance: false,
			taxes: false,
			savings: false
		},
		commerce: {
			department: false,
			price: false,
			product: false,
			isbn: false
		},
		vehicle: {
			type: false,
			color: false,
			manufacturer: false,
			model: false,
			fuel: false
		},
		institution: {
			fees: false,
			campus: false,
			location: false,
			fields: false
		},
		animals: {
			cat: false,
			dog: false,
			fish: false,
			snake: false,
			horse: false
		}
	};
	console.info(form);
	function generate() {
		let [key, value] = Object.entries(form);
		let [entry, data] = Object.entries(value);
		for ([key, value] of Object.entries(form)) {
			for ([entry, data] of Object.entries(value)) {
				if (data === true) {
					const sub = entry;
					for (let i = 0; i <= DataCount; i++) {
						 function valueReturn(key, sub) {
							console.info(key, Object.entries(form));
							switch (key) {
								case 'firstName':
									return faker.person.firstName();

								case 'lastName':
									return faker.person.lastName();

								case 'fullName':
									return faker.person.fullName();

								case 'phoneNumber':
									return faker.key.phoneNumber();

								case 'sex':
									return faker.key.sex();

								case 'jobTitle':
									return faker.key.jobTitle();

								case 'jobType':
									return faker.key.jobType();

								case 'number':
									return faker.key.number();

								case 'city':
									return faker.key.city();

								case 'country':
									return faker.key.country();

								case 'countryCode':
									return faker.key.countryCode();

								case 'direction':
									return faker.key.direction();

								case 'street':
									return faker.key.street();

								case 'zipCode':
									return faker.key.zipCode();

								case 'birthdate':
									return faker.date.birthdate();

								case 'weekday':
									return faker.date.weekday();

								case 'text':
									return faker.lorem.text();

								case 'sentences':
									return faker.lorem.sentences();

								case 'word':
									return faker.lorem.word();

								default:
									return 'New Data';
							}
						}
					  testData = [valueReturn(sub)]; 
						

						console.log(testData);
					}
				}
			}
		}
	}

	function handleSubmit(event) {
		event.preventDefault();
		generate();

		// Form submission logic here for faker.{field}.{entry}();
		// You can use the 'fields', 'count', and 'format' variables
	}
	console.log(form);
</script>

<Heading tag="h3" class="mb-2 p-3 py-8 text-center"
	>Generate Data <Span highlight><br /></Span><Span gradient /></Heading
>
<div>
	<form id="inputForm" on:submit={handleSubmit}>
		<div
			class="py-8 px-4 mx-auto max-w-screen-xl items-center text-left grid gap-6 xs:grid-cols-1 sm:grid-cols-3 grid-cols-2 space-y-0"
		>
			<div>
				<p class="mb-4 font-semibold text-gray-900 dark:text-white">Person</p>
				<pre>{form.person.fullName},{form.person.firstName},{form.person.lastName}</pre>
				<ul
					class="w-48 bg-white rounded-lg border border-gray-200 dark:bg-gray-800 dark:border-gray-600 divide-y divide-gray-200 dark:divide-gray-600"
				>
					<li>
						<Checkbox
							bind:checked={form.person.fullName}
							name="fields"
							value="full_name"
							id="full_name"
							class="p-1.5">Full Name</Checkbox
						>
					</li>
					<li>
						<Checkbox
							bind:checked={form.person.firstName}
							name="fields"
							value="first_name"
							id="first_name"
							class="p-1.5">First Name</Checkbox
						>
					</li>
					<li>
						<Checkbox
							bind:checked={form.person.middleName}
							name="fields"
							value="middle_name"
							id="middle_name"
							class="p-1.5">Middle Name</Checkbox
						>
					</li>
					<li>
						<Checkbox
							bind:checked={form.person.lastName}
							name="fields"
							value="last_name"
							id="last_name"
							class="p-1.5">Last Name</Checkbox
						>
					</li>
					<li>
						<Checkbox
							bind:checked={form.person.gender}
							name="fields"
							value="gender"
							id="gender"
							class="p-1.5">Gender</Checkbox
						>
					</li>
					<li>
						<Checkbox
							bind:checked={form.person.phoneNumber}
							name="fields"
							value="phone_number"
							id="phone_number"
							class="p-1.5">Phone Number</Checkbox
						>
					</li>
					<li>
						<Checkbox
							bind:checked={form.person.zodiacSign}
							name="fields"
							value="zodiac_sign"
							id="zodiac_sign"
							class="p-1.5">Zodiac Sign</Checkbox
						>
					</li>
				</ul>
			</div>
			<div>
				<p class="mb-4 font-semibold text-gray-900 dark:text-white">Finance</p>
				<ul
					class="w-48 bg-white rounded-lg border border-gray-200 dark:bg-gray-800 dark:border-gray-600 divide-y divide-gray-200 dark:divide-gray-600"
				>
					<li>
						<Checkbox
							bind:checked={form.finance.salary}
							name="fields"
							value="salary"
							id="salary"
							class="p-1.5">Salary</Checkbox
						>
					</li>
					<li>
						<Checkbox
							bind:checked={form.finance.insurance}
							name="fields"
							value="insurance"
							id="insurance"
							class="p-1.5">Insurance</Checkbox
						>
					</li>
					<li>
						<Checkbox
							bind:checked={form.finance.taxes}
							name="fields"
							value="taxes"
							id="taxes"
							class="p-1.5">Taxes</Checkbox
						>
					</li>
					<li>
						<Checkbox
							bind:checked={form.finance.savings}
							name="fields"
							value="salary"
							id="taxes"
							class="p-1.5">Savings</Checkbox
						>
					</li>
				</ul>
			</div>
			<div>
				<p class="mb-4 font-semibold text-gray-900 dark:text-white">Commerce</p>
				<ul
					class="w-48 bg-white rounded-lg border border-gray-200 dark:bg-gray-800 dark:border-gray-600 divide-y divide-gray-200 dark:divide-gray-600"
				>
					<li>
						<Checkbox
							bind:checked={form.commerce.department}
							name="fields"
							value="department"
							id="department"
							class="p-1.5">Department</Checkbox
						>
					</li>
					<li>
						<Checkbox
							bind:checked={form.commerce.price}
							name="fields"
							value="price"
							id="price"
							class="p-1.5">Price</Checkbox
						>
					</li>
					<li>
						<Checkbox
							bind:checked={form.commerce.product}
							name="fields"
							value="product"
							id="product"
							class="p-1.5">Product</Checkbox
						>
					</li>
					<li>
						<Checkbox
							bind:checked={form.commerce.isbn}
							name="fields"
							value="isbn"
							id="isbn"
							class="p-1.5">isbn</Checkbox
						>
					</li>
				</ul>
			</div>
			<div>
				<p class="mb-4 font-semibold text-gray-900 dark:text-white">Vehicle</p>
				<ul
					class="w-48 bg-white rounded-lg border border-gray-200 dark:bg-gray-800 dark:border-gray-600 divide-y divide-gray-200 dark:divide-gray-600"
				>
					<li>
						<Checkbox
							bind:checked={form.vehicle.type}
							name="fields"
							value="type"
							id="type"
							class="p-1.5">Type</Checkbox
						>
					</li>
					<li>
						<Checkbox
							bind:checked={form.vehicle.color}
							name="fields"
							value="color"
							id="color"
							class="p-1.5">Color</Checkbox
						>
					</li>
					<li>
						<Checkbox
							bind:checked={form.vehicle.manufacturer}
							name="fields"
							value="manufacturer"
							id="manufacturer"
							class="p-1.5">Manufacturer</Checkbox
						>
					</li>
					<li>
						<Checkbox
							bind:checked={form.vehicle.model}
							name="fields"
							value="model"
							id="model"
							class="p-1.5">Model</Checkbox
						>
					</li>
					<li>
						<Checkbox
							bind:checked={form.vehicle.fuel}
							name="fields"
							value="fuel"
							id="fuel"
							class="p-1.5">Fuel</Checkbox
						>
					</li>
				</ul>
			</div>
			<div>
				<p class="mb-4 font-semibold text-gray-900 dark:text-white">Institution</p>
				<ul
					class="w-48 bg-white rounded-lg border border-gray-200 dark:bg-gray-800 dark:border-gray-600 divide-y divide-gray-200 dark:divide-gray-600"
				>
					<li>
						<Checkbox
							bind:checked={form.institution.fees}
							name="fields"
							value="fees"
							id="fees"
							class="p-1.5">Fees</Checkbox
						>
					</li>
					<li>
						<Checkbox
							bind:checked={form.institution.campus}
							name="fields"
							value="campus"
							id="campus"
							class="p-1.5">Campus</Checkbox
						>
					</li>
					<li>
						<Checkbox
							bind:checked={form.institution.location}
							name="fields"
							value="location"
							id="location"
							class="p-1.5">Location</Checkbox
						>
					</li>
					<li>
						<Checkbox
							bind:checked={form.institution.fields}
							name="fields"
							value="fields"
							id="fields"
							class="p-1.5">Fields</Checkbox
						>
					</li>
				</ul>
			</div>
			<div>
				<p class="mb-4 font-semibold text-gray-900 dark:text-white">Animals</p>
				<ul
					class="w-48 bg-white rounded-lg border border-gray-200 dark:bg-gray-800 dark:border-gray-600 divide-y divide-gray-200 dark:divide-gray-600"
				>
					<li>
						<Checkbox
							bind:checked={form.animals.cat}
							name="fields"
							value="cat"
							id="cat"
							class="p-1.5">Cat</Checkbox
						>
					</li>
					<li>
						<Checkbox
							bind:checked={form.animals.dog}
							name="fields"
							value="dog"
							id="dog"
							class="p-1.5">Dog</Checkbox
						>
					</li>
					<li>
						<Checkbox
							bind:checked={form.animals.fish}
							name="fields"
							value="fish"
							id="fish"
							class="p-1.5">Fish</Checkbox
						>
					</li>
					<li>
						<Checkbox
							bind:checked={form.animals.snake}
							name="fields"
							value="snake"
							id="snake"
							class="p-1.5">Snake</Checkbox
						>
					</li>
					<li>
						<Checkbox
							bind:checked={form.animals.horse}
							name="fields"
							value="horse"
							id="horse"
							class="p-1.5">Horse</Checkbox
						>
					</li>
				</ul>
			</div>

			<div class="mb-6">
				<Label class="block mb-2">
					<span>Count of Data</span>
					<NumberInput bind:value={DataCount} />
				</Label>
				<br />
				<Label
					>Select a Format
					<Select items={FormatTypes} bind:value={FormatType} />
					<!-- on:change={handleSubmit(event)  -->
				</Label>
			</div>
			<Input
				class="border-2 border-gray-500 rounded-lg"
				id="submit"
				type="submit"
				value="GENERATE DATA"
			/>
		</div>
	</form>
	<br />
	<div>
		{#each Object.entries(form) as [field, stat]}
			<pre>{field}</pre>
			{#each Object.entries(stat) as [entry, data]}
				<pre>{entry}={data}</pre>
				{#if data == true}
					<pre> faker.{field}.{entry}()</pre>
				{/if}
			{/each}
		{/each}
		<textarea
			value={console.info(testData)}
			placeholder="Generated Data"
			readonly
			class="custom-scrollbar focus:outline-0 focus:shadow-none dark:text-gray-500 block p-2.5 bg-white bg-transparent w-full h-full text-sm text-gray-500 border-0"
		/>
	</div>
	<br />
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


<script>
  import { onMount } from "svelte";
  import { Heading, Input, NumberInput,Span,Label, Select } from 'flowbite-svelte';
  import { Checkbox } from 'flowbite-svelte';
 // Function to handle the form submission
 function handleSubmit(event) {
   console.log(data); }
   let value = 5;
   import {  InputAddon, ButtonGroup, Button, Dropdown, DropdownItem } from 'flowbite-svelte';
   import { ChevronDownSolid } from 'flowbite-svelte-icons';

</script>
 
 <Heading tag="h3" class="mb-2 p-3 py-8 text-center">Generate Data <Span highlight><br></Span> <Span gradient></Span></Heading>
 <div>
   <form id="inputForm" on:submit|preventDefault={handleSubmit}>
   <div class="py-8 px-4 mx-auto max-w-screen-xl items-center text-left grid gap-6 xs:grid-cols-1 sm:grid-cols-3 grid-cols-2 space-y-0 ">
  <div>
    <p class="mb-4 font-semibold text-gray-900 dark:text-white">Personal</p>
    <ul class="w-48 bg-white rounded-lg border border-gray-200 dark:bg-gray-800 dark:border-gray-600 divide-y divide-gray-200 dark:divide-gray-600">
      <li><Checkbox name="fields" value="name" id="name" class="p-1.5">Name</Checkbox></li>
      <li><Checkbox name="fields" value="email" id="email" class="p-1.5">Email</Checkbox></li>
      <li><Checkbox name="fields" value="phone_number" id="phone_number" class="p-1.5">Phone Number</Checkbox></li>
      <li><Checkbox name="fields" value="address" id="address" class="p-1.5">Address</Checkbox></li>
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
   <p class="mb-4 font-semibold text-gray-900 dark:text-white">Job</p>
    <ul class="w-48 bg-white rounded-lg border border-gray-200 dark:bg-gray-800 dark:border-gray-600 divide-y divide-gray-200 dark:divide-gray-600">
    <li><Checkbox name="fields" value="IT" id="IT" class="p-1.5">IT</Checkbox></li>
    <li><Checkbox name="fields" value="management" id="management" class="p-1.5">Management</Checkbox></li>
    <li><Checkbox name="fields" value="marketing" id="marketing" class="p-1.5">Marketing</Checkbox></li>
    <li><Checkbox name="fields" value="business" id="business" class="p-1.5">Business</Checkbox></li>
    </ul>
  </div>
  <div>
    <p class="mb-4 font-semibold text-gray-900 dark:text-white">Travel</p>
     <ul class="w-48 bg-white rounded-lg border border-gray-200 dark:bg-gray-800 dark:border-gray-600 divide-y divide-gray-200 dark:divide-gray-600">
     <li><Checkbox name="fields" value="budget" id="budget" class="p-1.5">Budget</Checkbox></li>
     <li><Checkbox name="fields" value="days" id="days" class="p-1.5">Number of days</Checkbox></li>
     <li><Checkbox name="fields" value="location" id="location" class="p-1.5">Location</Checkbox></li>
     <li><Checkbox name="fields" value="tourist_attractions" id="tourist_attractions" class="p-1.5">Tourist Attractions</Checkbox></li>
     </ul>
 </div> 
 <!--<div>
    <p class="mb-4 font-semibold text-gray-900 dark:text-white">Products</p>
     <ul class="w-48 bg-white rounded-lg border border-gray-200 dark:bg-gray-800 dark:border-gray-600 divide-y divide-gray-200 dark:divide-gray-600">
     <li><Checkbox class="p-1.5">svelte</Checkbox></li>
     <li><Checkbox class="p-1.5">Vue JS</Checkbox></li>
     <li><Checkbox class="p-1.5">React</Checkbox></li>
     <li><Checkbox class="p-1.5">Angular</Checkbox></li>
     </ul>
 </div> -->
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
  <p class="mb-4 font-semibold text-gray-900 dark:text-white">Purchase</p>
   <ul class="w-48 bg-white rounded-lg border border-gray-200 dark:bg-gray-800 dark:border-gray-600 divide-y divide-gray-200 dark:divide-gray-600">
   <li><Checkbox name="fields" value="product" id="product" class="p-1.5">Product</Checkbox></li>
   <li><Checkbox name="fields" value="price" id="price" class="p-1.5">Price</Checkbox></li>
   <li><Checkbox name="fields" value="quality" id="quality" class="p-1.5">Quality</Checkbox></li>
   <li><Checkbox name="fields" value="quantity" id="quantity" class="p-1.5">Quantity</Checkbox></li>
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
      <Button color="none" class="flex-shrink-0 text-gray-900 bg-gray-100 border border-gray-300 dark:border-gray-700 dark:text-white hover:bg-gray-200 focus:ring-gray-300 dark:bg-gray-600 dark:hover:bg-gray-700 dark:focus:ring-gray-800">
       Language <ChevronDownSolid class="w-3 h-3 ml-2 text-white dark:text-white" />
      </Button>
      <Dropdown>
        <DropdownItem>Json</DropdownItem>
        <DropdownItem>CSV</DropdownItem>
        <DropdownItem>TV</DropdownItem>
        <DropdownItem>html</DropdownItem>
      </Dropdown>
      <Input placeholder="Select" />
  
    </ButtonGroup>
</div>
</div>
</div>
</form>
</div>



<!--
<div class="tile position-relative text-center">
    <div class="main-info col-md-8 p-lg-5 mx-auto my-3">
        <Heading tag="h1" class="mb-4">Welcome to the <Span highlight>#Ultimate <br></Span> <Span gradient>Fake Data Generator!</Span></Heading>
    <p class="lead font-weight-normal">Generate fake data, or build your API query here.</p>
    <form id="fake-form" action="/console/" method="GET">
    <div class="text-center ">
    <label for="exampleFormControlSelect2"><strong>Generated Data</strong></label>
    <div class="form-row">
    <div class="col">
    <div class="custom-control custom-checkbox">
    <input name="fields" value="name" id="name" type="checkbox" class="custom-control-input field">
    <label for="name" class="custom-control-label">Names</label>
    </div>
    <div class="custom-control custom-checkbox">
    <input name="fields" value="email" id="email" type="checkbox" class="custom-control-input field">
    <label for="email" class="custom-control-label">Emails</label>
    </div>
    <div class="custom-control custom-checkbox">
    <input name="fields" value="address" id="address" type="checkbox" class="custom-control-input field">
    <label for="address" class="custom-control-label">Addresses</label>
    </div>
    <div class="custom-control custom-checkbox">
    <input name="fields" value="date" id="date" type="checkbox" class="custom-control-input field">
    <label for="date" class="custom-control-label">Dates</label>
    </div>
    </div>
    <div class="col">
    <div class="custom-control custom-checkbox">
    <input name="fields" value="ssn" id="ssn" type="checkbox" class="custom-control-input field">
    <label for="ssn" class="custom-control-label">SSNs</label>
    </div>
    <div class="custom-control custom-checkbox">
    <input name="fields" value="company_email" id="company_email" type="checkbox" class="custom-control-input field">
    <label for="company_email" class="custom-control-label">Corporate Emails</label>
    </div>
    <div class="custom-control custom-checkbox">
    <input name="fields" value="city" id="city" type="checkbox" class="custom-control-input field">
    <label for="city" class="custom-control-label">Cities</label>
    </div>
    <div class="custom-control custom-checkbox">
    <input name="fields" value="job" id="job" type="checkbox" class="custom-control-input field">
    <label for="job" class="custom-control-label">Jobs</label>
    </div>
    </div>
    <div class="col">
    <div class="custom-control custom-checkbox">
    <input name="fields" value="license_plate" id="license_plate" type="checkbox" class="custom-control-input field">
    <label for="license_plate" class="custom-control-label">License Plates</label>
    </div>
    <div class="custom-control custom-checkbox">
    <input name="fields" value="date" id="date" type="checkbox" class="custom-control-input field">
    <label for="date" class="custom-control-label">Phone Number</label>
    </div>
    <div class="custom-control custom-checkbox">
    <input name="fields" value="company" id="company" type="checkbox" class="custom-control-input field">
    <label for="company" class="custom-control-label">Companies</label>
    </div>
    <div class="custom-control custom-checkbox">
    <input name="fields" value="url" id="url" type="checkbox" class="custom-control-input field">
    <label for="url" class="custom-control-label">Websites</label>
    </div>
    </div>
    </div>
    <div class="form-group">
    <label for="formControlRange">Data Points</label> <strong>(e.g. 1 - 2000)</strong>
    <input class="form-control" type="number" value="10" id="count" name="count" min="10" max="2000">
    </div>
    <div class="form-group">
    <label for="exampleFormControlSelect1">Format</label>
    <select class="form-control" id="format" name="format">
    <option>html</option>
    <option>csv</option>
    <option>json</option>
    </select>
    </div>
    </div>
    <input type="submit" class="btn btn-primary" value="Generate Data">
    
    </form>
    </div>
    <div class="product-device shadow-sm d-none d-md-block"></div>
    <div class="product-device product-device-2 shadow-sm d-none d-md-block"></div>
    </div>
    
    <div class="tile position-relative overflow-hidden p-3 p-md-5 m-md-3 text-center bg-light">
    <div id="data" class="d-md-flex flex-md-equal w-100 my-md-3">
    </div>
    </div>
    
-->
    

    
    <!--<script>
      // this is the id of the form
    
    $("#fake-form").submit(function(e) {
    
    e.preventDefault(); // avoid to execute the actual submit of the form.
    
    var form = $(this);
    var url = form.attr('action');
    var api = "https://api.faker.dev/table";
    var data = form.serializeArray().reduce(function(obj, item) {
       // Collapsing Keys
        obj[item.name] = obj[item.name]?[obj[item.name], item.value].join(','):item.value;
        return obj;
    }, {});
    console.log(data);
    $.ajax({
           type: "GET",
           url: api,
           data: data,
           success: function(data)
           {
               $("#data").html(data);
           }
         });
    });
    </script>
    -->
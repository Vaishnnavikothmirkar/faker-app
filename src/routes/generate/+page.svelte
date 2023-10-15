
<script>
    import { onMount } from "svelte";
    import { Heading, Input, Span,Label, Select } from 'flowbite-svelte';
    import { Checkbox } from 'flowbite-svelte';
   // Function to handle the form submission
   export let dataFormats = ["JSON", "CSV", "JavaScript", "TSV"];
   let format = "JSON";
   function handleSubmit(event) {
     console.log(data); }
 </script>
 
 <Heading tag="h3" class="mb-2 p-3 py-8 text-center">Generate Data <Span highlight><br></Span> <Span gradient></Span></Heading>
 <div>
   <form id="inputForm" on:submit|preventDefault={handleSubmit}>
   <div class="py-8 px-4 mx-auto max-w-screen-xl items-center text-left grid gap-6 xs:grid-cols-1 sm:grid-cols-3 grid-cols-2 space-y-0 ">
  <div>
    <p class="mb-4 font-semibold text-gray-900 dark:text-white">Technology</p>
    <ul class="w-48 bg-white rounded-lg border border-gray-200 dark:bg-gray-800 dark:border-gray-600 divide-y divide-gray-200 dark:divide-gray-600">
      <li><Checkbox class="p-1.5">svelte</Checkbox></li>
      <li><Checkbox class="p-1.5">Vue JS</Checkbox></li>
      <li><Checkbox class="p-1.5">React</Checkbox></li>
      <li><Checkbox class="p-1.5">Angular</Checkbox></li>
    </ul> 
 </div>
 <div>
    <p class="mb-4 font-semibold text-gray-900 dark:text-white">Finance</p>
    <ul class="w-48 bg-white rounded-lg border border-gray-200 dark:bg-gray-800 dark:border-gray-600 divide-y divide-gray-200 dark:divide-gray-600">
      <li><Checkbox class="p-1.5">svelte</Checkbox></li>
      <li><Checkbox class="p-1.5">Vue JS</Checkbox></li>
      <li><Checkbox class="p-1.5">React</Checkbox></li>
      <li><Checkbox class="p-1.5">Angular</Checkbox></li>
    </ul>
 </div>
<div>
   <p class="mb-4 font-semibold text-gray-900 dark:text-white">Personal</p>
    <ul class="w-48 bg-white rounded-lg border border-gray-200 dark:bg-gray-800 dark:border-gray-600 divide-y divide-gray-200 dark:divide-gray-600">
    <li><Checkbox class="p-1.5">svelte</Checkbox></li>
    <li><Checkbox class="p-1.5">Vue JS</Checkbox></li>
    <li><Checkbox class="p-1.5">React</Checkbox></li>
    <li><Checkbox class="p-1.5">Angular</Checkbox></li>
    </ul>
  </div>
  <div>
    <p class="mb-4 font-semibold text-gray-900 dark:text-white">location</p>
     <ul class="w-48 bg-white rounded-lg border border-gray-200 dark:bg-gray-800 dark:border-gray-600 divide-y divide-gray-200 dark:divide-gray-600">
     <li><Checkbox class="p-1.5">svelte</Checkbox></li>
     <li><Checkbox class="p-1.5">Vue JS</Checkbox></li>
     <li><Checkbox class="p-1.5">React</Checkbox></li>
     <li><Checkbox class="p-1.5">Angular</Checkbox></li>
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
    <p class="mb-4 font-semibold text-gray-900 dark:text-white">Time Based</p>
     <ul class="w-48 bg-white rounded-lg border border-gray-200 dark:bg-gray-800 dark:border-gray-600 divide-y divide-gray-200 dark:divide-gray-600">
     <li><Checkbox class="p-1.5">svelte</Checkbox></li>
     <li><Checkbox class="p-1.5">Vue JS</Checkbox></li>
     <li><Checkbox class="p-1.5">React</Checkbox></li>
     <li><Checkbox class="p-1.5">Angular</Checkbox></li>
     </ul>
 </div>
 <br>
 <br>
  <div class="mb-6">
  <Label for="default-input" class="block mb-2">Count of Data</Label>
  <Input id="count" placeholder="Count" />
  <br>
  <div>
    <Label for="format">Data Format :</Label>
    <Select
    name="dataFormat"
    class="dataFormat"
    bind:value={dataFormats}
    >
    {#each dataFormats as format}
        <option class="format" {format} > {format} </option>
    {/each}
    </Select>
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
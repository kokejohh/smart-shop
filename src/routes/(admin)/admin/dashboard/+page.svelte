<script lang="ts">
	import Density from '../../../../components/admin/Density.svelte';
	import PeekTime from '../../../../components/admin/PeekTime.svelte';
</script>

<div class="grid grid-cols-1 place-content-center place-items-center gap-8 lg:grid-cols-2">
	<div class="card h-42 w-full place-self-end bg-base-100 px-8 shadow-sm card-md indicator">
		<div class="indicator-item badge badge-info badge-xl">
  <svg class="size-[1em]" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><g fill="currentColor" stroke-linejoin="miter" stroke-linecap="butt"><circle cx="12" cy="12" r="10" fill="none" stroke="currentColor" stroke-linecap="square" stroke-miterlimit="10" stroke-width="2"></circle><path d="m12,17v-5.5c0-.276-.224-.5-.5-.5h-1.5" fill="none" stroke="currentColor" stroke-linecap="square" stroke-miterlimit="10" stroke-width="2"></path><circle cx="12" cy="7.25" r="1.25" fill="currentColor" stroke-width="2"></circle></g></svg>
</div>
		<div class="card-body">
			<h2 class="card-title">Total Sales Today</h2>
			<p class="flex items-center text-4xl font-semibold">฿ 42,590</p>
		</div>
	</div>

	<div class="card h-42 w-full bg-base-100 px-8 shadow-sm card-md indicator">
		<div class="indicator-item badge badge-warning badge-xl">
			<svg class="size-[1em]" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 18 18"><g fill="currentColor"><path d="M7.638,3.495L2.213,12.891c-.605,1.048,.151,2.359,1.362,2.359H14.425c1.211,0,1.967-1.31,1.362-2.359L10.362,3.495c-.605-1.048-2.119-1.048-2.724,0Z" fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5"></path><line x1="9" y1="6.5" x2="9" y2="10" fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5"></line><path d="M9,13.569c-.552,0-1-.449-1-1s.448-1,1-1,1,.449,1,1-.448,1-1,1Z" fill="currentColor" data-stroke="none" stroke="none"></path></g></svg>
		</div>
		<div class="card-body">
			<h2 class="card-title">Urgent Alert</h2>
			<p class="flex items-center text-4xl font-semibold">3 Items</p>
		</div>
	</div>
	<div class="card h-42 w-full bg-base-100 px-8 shadow-sm card-md indicator">
		<div class="indicator-item badge badge-success badge-xl">
			<svg class="size-[1em]" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><g fill="currentColor" stroke-linejoin="miter" stroke-linecap="butt"><circle cx="12" cy="12" r="10" fill="none" stroke="currentColor" stroke-linecap="square" stroke-miterlimit="10" stroke-width="2"></circle><polyline points="7 13 10 16 17 8" fill="none" stroke="currentColor" stroke-linecap="square" stroke-miterlimit="10" stroke-width="2"></polyline></g></svg>
		</div>
		<div class="card-body">
			<h2 class="card-title">Successful Order</h2>
			<p class="flex items-center text-4xl font-semibold">1,204 Bills</p>
		</div>
	</div>

	<div class="card h-42 w-full bg-base-100 px-8 shadow-sm card-md indicator">
		<div class="indicator-item badge badge-error badge-xl">
			Live		
		</div>
		<div class="card-body">
			<h2 class="card-title">Customers in The Store (Live)</h2>
			<p class="flex items-center text-4xl font-semibold">2</p>
		</div>
	</div>

	<div class="card col-span-1 h-54 w-full bg-base-100 px-8 shadow-sm card-md lg:col-span-2">
		<div class="card-body">
			<div class="sticky flex justify-between">
				<h2 class="card-title">Stock Alert</h2>
				<div class="badge badge-error">Critical</div>
			</div>
			<div class="h-42 space-y-2 overflow-y-auto text-lg">
				<div class="flex justify-between rounded-lg bg-base-300 p-2">
					<div class="flex-1">
						<div class="badge badge-xs badge-error"></div>
						Sandwidch Ham Cheese
					</div>
					<div class="flex-1 text-center text-error">Out of Stock</div>
					<div class="flex-1 text-end">0</div>
				</div>
				<div class="flex justify-between rounded-lg bg-base-300 p-2">
					<div class="flex-1">
						<div class="badge badge-xs badge-warning"></div>
						Mango
					</div>
					<div class="flex-1 text-center text-warning">Low Stock</div>
					<div class="flex-1 text-end">2</div>
				</div>
			</div>
		</div>
	</div>
	<div class="card w-full bg-base-100 px-8 shadow-sm card-md">
		<div class="card-body">
			<h2 class="card-title">Peak Time</h2>
			<select class="select w-1/3 shrink-0" name="fruits" id="fruits">
				<option value="apple" selected>Today</option>
				<option value="banana">Yesterday</option>
			</select>
			<PeekTime />
		</div>
	</div>
	<div class="card w-full bg-base-100 px-8 shadow-sm card-md">
		<div class="card-body">
			<h2 class="card-title">Customer Density</h2>
			<select class="select w-1/3 shrink-0" name="fruits" id="fruits">
				<option value="apple" selected>Today</option>
				<option value="banana">Yesterday</option>
			</select>
			<Density />
		</div>
	</div>
</div>

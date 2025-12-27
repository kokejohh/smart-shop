<script lang="ts">
	import a1 from '$lib/images/1.jpg';
	import a2 from '$lib/images/2.png';
	import a3 from '$lib/images/3.png';

	let selectProducts = $state([]);

	function selectAll() {
		console.log(selectProducts)
		selectProducts = [];
	}

	function resetFilter() {
		selectProducts = [];
	}
</script>

<h1 class="text-2xl font-bold">Warehouse & Inventory</h1>
<br />
<div class="grid grid-cols-1 place-content-center place-items-center gap-6 lg:grid-cols-2">
	<div class="card h-32 w-full place-self-end bg-base-100 px-8 shadow-sm card-md">
		<div class="card-body">
			<div class="flex h-full items-center">
				<h2 class="card-title flex-1 text-2xl">Total Products</h2>
				<div class="flex-1 text-center text-xl font-bold">
					<p>1,240</p>
					<p>Items</p>
				</div>
			</div>
		</div>
	</div>

	<div class="card h-32 w-full place-self-end bg-base-100 px-8 shadow-sm card-md">
		<div class="card-body">
			<div class="flex h-full items-center">
				<h2 class="card-title flex-1 text-2xl">Total Stock Value</h2>
				<div class="flex-1 text-center text-xl font-bold">
					<p>฿ 485K</p>
					<p>Est. Value</p>
				</div>
			</div>
		</div>
	</div>

	<div class="card h-32 w-full place-self-end bg-base-100 px-8 shadow-sm card-md">
		<div class="card-body">
			<div class="flex h-full items-center">
				<h2 class="card-title flex-1 text-2xl text-warning">Low Stock Alerts</h2>
				<div class="flex-1 text-center text-xl font-bold">
					<p>12</p>
					<p>Items needs restock</p>
				</div>
			</div>
		</div>
	</div>

	<div class="card h-32 w-full place-self-end bg-base-100 px-8 shadow-sm card-md">
		<div class="card-body">
			<div class="flex h-full items-center">
				<h2 class="card-title flex-1 text-2xl text-error">Out of Stock</h2>
				<div class="flex-1 text-center text-xl font-bold">
					<p>5</p>
					<p>Currently unavailable</p>
				</div>
			</div>
		</div>
	</div>

	<div class="card col-span-1 w-full bg-base-100 shadow-sm card-md lg:col-span-2">
		<div class="card-body">
			<div class="flex justify-between">
				<label class="input">
					<svg class="h-[1em] opacity-50" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
						<g
							stroke-linejoin="round"
							stroke-linecap="round"
							stroke-width="2.5"
							fill="none"
							stroke="currentColor"
						>
							<circle cx="11" cy="11" r="8"></circle>
							<path d="m21 21-4.3-4.3"></path>
						</g>
					</svg>
					<input type="search" class="grow" placeholder="Search" />
				</label>
				<form>
					<input class="btn btn-outline" type="checkbox" name="products" checked={selectProducts.length === 0} onclick={selectAll} aria-label="All" />
					<input class="btn btn-outline" type="checkbox" name="products" bind:group={selectProducts} value="Beverage" aria-label="Beverage" />
					<input class="btn btn-outline" type="checkbox" name="products" bind:group={selectProducts} value="Food" aria-label="Food" />
					<input class="btn btn-outline" type="checkbox" name="products" bind:group={selectProducts} value="Snacks" aria-label="Snacks" />
					<input class="btn btn-outline" type="checkbox" name="products" bind:group={selectProducts} value="Household" aria-label="Household" />
					<input class="btn btn-outline" type="checkbox" name="products" bind:group={selectProducts} value="Health" aria-label="Health" />
					<input class="btn btn-outline" type="checkbox" name="products" bind:group={selectProducts} value="Low Stock" aria-label="Low Stock" />
					<input class="btn btn-outline btn-square" type="reset" onclick={resetFilter} value="×" />
				</form>
			</div>
			<div class="overflow-x-auto">
				<table class="table text-center">
					<!-- head -->
					<thead>
						<tr>
							<th>
								<label>
									<input type="checkbox" class="checkbox" />
								</label>
							</th>
							<th>Product Name</th>
							<th>Category</th>
							<th>Price</th>
							<th>Stock Qty</th>
							<th>Status</th>
							<th>Actions</th>
							<!-- <th></th> -->
						</tr>
					</thead>
					<tbody>
						<!-- row 1 -->
						<tr>
							<th>
								<label>
									<input type="checkbox" class="checkbox" />
								</label>
							</th>
							<td>
								<div class="flex items-center gap-3">
									<div class="avatar">
										<div class="mask h-16 w-16 mask-squircle">
											<img src={a1} alt="Avatar Tailwind CSS Component" />
										</div>
									</div>
									<div>
										<div class="font-bold">meiji</div>
										<div class="text-sm opacity-50">น้ำนมโค 100%</div>
									</div>
								</div>
							</td>
							<td>Beverage</td>
							<td>฿12.50 <br /> Cost: ฿9.00</td>
							<td>40</td>
							<td><div class="badge badge-error">Out of Stock</div></td>
							<th>
								<button class="btn btn-ghost btn-xs">details</button>
							</th>
						</tr>
						<!-- row 2 -->
						<tr>
							<th>
								<label>
									<input type="checkbox" class="checkbox" />
								</label>
							</th>
							<td>
								<div class="flex items-center gap-3">
									<div class="avatar">
										<div class="mask h-16 w-16 mask-squircle">
											<img class="object-contain" src={a2} alt="Avatar Tailwind CSS Component" />
										</div>
									</div>
									<div>
										<div class="font-bold">Lay's</div>
										<div class="text-sm opacity-50">รสมันฝรั่งแท้</div>
									</div>
								</div>
							</td>
							<td>Snacks</td>
							<td>฿30.00 <br /> Cost: ฿22.0</td>
							<td>29</td>
							<td><div class="badge badge-success">In Stock</div></td>
							<th>
								<button class="btn btn-ghost btn-xs">details</button>
							</th>
						</tr>
						<!-- row 3 -->
						<tr>
							<th>
								<label>
									<input type="checkbox" class="checkbox" />
								</label>
							</th>
							<td>
								<div class="flex items-center gap-3">
									<div class="avatar">
										<div class="mask h-16 w-16 mask-squircle">
											<img src={a3} alt="Avatar Tailwind CSS Component" />
										</div>
									</div>
									<div>
										<div class="font-bold">CRYSTAL</div>
										<div class="text-sm opacity-50">น้ำเปล่า</div>
									</div>
								</div>
							</td>
							<td>Beverage</td>
							<td>฿7.00 <br /> Cost: ฿4.50</td>
							<td>40</td>
							<td><div class="badge badge-success">In Stock</div></td>
							<th>
								<button class="btn btn-ghost btn-xs">details</button>
							</th>
						</tr>
					</tbody>
				</table>
			
			</div>	<div class="flex items-center justify-between px-6">
					<div>showing 1-3 of 400 items</div>
					<div class="join space-x-2">
						<button class="btn btn-disabled join-item">Previous</button>
						<button class="btn btn-active join-item">1</button>
						<button class="btn join-item">2</button>
						<button class="btn join-item">3</button>
						<button class="btn join-item">Next</button>
					</div>
				</div>
		</div>
	</div>
</div>

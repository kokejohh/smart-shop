<script lang="ts">
	import TargetGroup from '../../../../components/admin/TargetGroup.svelte';
</script>

<h1 class="text-2xl font-bold">Customer Information</h1>
<div>PDPA Complaint System ข้อมูลส่วนบุคคลถูกเข้ารหัส (End-to-End Encryption)</div>

<div class="grid grid-cols-1 gap-6 lg:grid-cols-3">
	<div class="card h-ful w-full bg-base-100 px-8 shadow-sm card-md lg:col-span-2">
		<div class="card-body">
			<h2 class="card-title">สินค้าที่ควรเติม</h2>
		</div>
	</div>

	<div class="card w-full bg-base-100 px-8 shadow-sm card-md">
		<div class="card-body">
			<h2 class="card-title">Target Group</h2>
			<TargetGroup />
			<div class="pointer-events-none absolute inset-0 flex flex-col items-center justify-center">
				<span class="text-2xl font-bold">1.2K</span>
				<span class="text-xs text-gray-500">Total</span>
			</div>
		</div>
	</div>

	<div class="card h-42 w-full bg-indigo-600 px-8 text-white shadow-sm card-md lg:col-span-3">
		<div class="flex h-full w-full items-center text-center">
			<div class="w-1/2 space-y-2 font-bold">
				<h2 class="text-2xl">Lifetime Value (LTV)</h2>
				<p class="text-4xl">850,200 บาท</p>
				<p class="text-xl">มูลค่าการซื้อรวมทั้งหมดของสมาชิกระดับ VIP</p>
			</div>
			<div class="divider divider-horizontal"></div>
			<div class="w-1/2 space-y-2 font-bold">
				<h2 class="text-xl">AI Suggestion</h2>
				<p class="text-2xl">
					ควรจัดโปรโมชั้น "ซื้อครบ 500 แถมกระเป๋าผ้า" <br /> เพื่อกระตุ้นยอดกลุ่ม VIP ให้ซื้อเพื่ม 15%
				</p>
			</div>
		</div>
	</div>

	<div class="card w-full bg-base-100 shadow-sm card-md lg:col-span-3">
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
							<th>Customer Info</th>
							<th>PDPA Status</th>
							<th>Segment</th>
							<th>Total Spend</th>
							<th>Top Purchase</th>
							<th>Last Visit</th>
							<th>Actions</th>
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
									<div class="btn avatar avatar-placeholder btn-circle w-10 btn-ghost">
										<div class="w-full rounded-full bg-neutral text-neutral-content">
											<span>สจ</span>
										</div>
									</div>
									<div>
										<div class="font-bold">สมชาย ใจดี</div>
										<div class="text-sm opacity-50">C-1042</div>
									</div>
								</div>
							</td>
							<td><div class="badge badge-success">Consent Given</div></td>
							<td><div class="badge badge-primary">Office Worker</div></td>
							<td>฿654</td>
							<td>เครื่องดื่ม (Coffee)</td>
							<td>Today, 10:30</td>
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
									<div
										tabindex="0"
										role="button"
										class="btn avatar avatar-placeholder btn-circle w-10 btn-ghost"
									>
										<div class="w-full rounded-full bg-neutral text-neutral-content">
											<span>HN</span>
										</div>
									</div>
									<div>
										<div class="font-bold">Hidden Name</div>
										<div class="text-sm opacity-50">C-8821</div>
									</div>
								</div>
							</td>
							<td><div class="badge badge-error">Partial</div></td>
							<td><div class="badge badge-secondary">Casual</div></td>
							<td>฿400</td>
							<td>ขนมขบเคี้ยว</td>
							<td>Yesterday</td>
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
									<div
										tabindex="0"
										role="button"
										class="btn avatar avatar-placeholder btn-circle w-10 btn-ghost"
									>
										<div class="w-full rounded-full bg-neutral text-neutral-content">
											<span>HN</span>
										</div>
									</div>
									<div>
										<div class="font-bold">Hidden Name</div>
										<div class="text-sm opacity-50">C-4401</div>
									</div>
								</div>
							</td>
							<td><div class="badge badge-neutral">No Data</div></td>
							<td><div class="badge badge-accent">New</div></td>
							<td>฿120</td>
							<td>อาหารพร้อมทาน</td>
							<td>Today, 12:00</td>
							<th>
								<button class="btn btn-ghost btn-xs">details</button>
							</th>
						</tr>
					</tbody>
				</table>
			</div>
			<div class="flex items-center justify-between px-6">
				<div>showing 1-3 of 1423 customers</div>
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

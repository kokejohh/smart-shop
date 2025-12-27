<script lang="ts">
</script>

<h1 class="text-2xl font-bold">System Settings</h1>
<br />
<div class="grid grid-cols-1 lg:grid-cols-2 place-content-center place-items-center gap-6">
	<div class="card w-full h-64 place-self-end bg-base-100 px-8 shadow-sm card-md">
		<div class="card-body">
			<h2 class="card-title text-2xl">ข้อมูลร้านค้า</h2>
			<br>
			<label class="text-xl">
				<span class="font-bold">ชื่อร้านค้า :</span>
				<input type="text" class="input w-full text-xl" value="Smart Shop - สาขาหลัก" readonly/>
			</label>
			<label class="text-xl">
				<span class="font-bold">เวลาเปิด : </span><br>
				<input type="time" class="input w-1/3 lg:w-32 text-xl" value="08:00" readonly/><span class="font-bold mx-4"> - </span> 
				<input type="time" class="input w-1/3 lg:w-32 text-xl" value="23:00" readonly/>
			</label>
		</div>
	</div>

	<div class="card w-full h-64 place-self-end bg-base-100 px-8 shadow-sm card-md">
		<div class="card-body">
			<h2 class="card-title text-2xl">ระบบ AI & ความปลอดภัย</h2>
			<div class="text-xl">ความไวในการตรวจจับ (AI Sensitivity)</div>
			<div class="w-full mt-8">
				<input type="range" min="0" max="100" value="25" class="range w-full" step="25" />
				<div class="mt-2 flex justify-between px-2.5 text-xs">
					<span>|</span>
					<span>|</span>
					<span>|</span>
					<span>|</span>
					<span>|</span>
				</div>
				<div class="mt-2 flex justify-between px-2.5 text-xs">
					<span>1</span>
					<span>2</span>
					<span>3</span>
					<span>4</span>
					<span>5</span>
				</div>
			</div>
		</div>
	</div>

	<div class="card w-full place-self-end bg-base-100 p-8 shadow-sm card-md lg:col-span-2">
		<div class="card-body text-lg">
			<div class="flex flex-wrap justify-around">
				<div class="flex flex-col w-128">
					<div class="flex justify-between h-24">
						<div>
							เปิดใช้งานระบบจดจำใบหน้า (Face ID)
							<br> ระบุตัวตนสมาชิกอัตโนมัติ
						</div>
						<input type="checkbox" checked={true} class="toggle toggle-success toggle-xl" />
					</div>
					<div class="flex justify-between h-24">
						<div>
							ตรวจจับการขโมยสินค้า (Anti-Theft)
							<br> แจ้งเตือนทันทีเมื่อหยิบของแล้วไม่จ่าย
						</div>
						<input type="checkbox" checked={true} class="toggle toggle-success toggle-xl" />
					</div>
				</div>
				<div class="flex flex-col w-128">
					<div class="flex justify-between h-24">
						<div>
							แจ้งเตือนของหมดสต๊อก
						</div>
						<input type="checkbox" checked={true} class="toggle toggle-success toggle-xl" />
					</div>
					<div class="flex justify-between h-24">
						<div>
							แจ้งเตือนสรุปยอดขายรายวัน
						</div>
						<input type="checkbox" checked={true} class="toggle toggle-success toggle-xl" />
					</div>
				</div>
				<div class="flex flex-col w-52 bg-green-600 items-center justify-center space-y-8 rounded-xl">
					<div class="text-white">เชื่อมต่อ Line Notify</div>
					<button class="btn btn-white btn-sm w-2/3">เชื่อมต่อแล้ว</button>
				</div>
			</div>
		</div>
	</div>
</div>

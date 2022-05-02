<script>
	async function getDate() {
		const res = await fetch('https://api.github.com/repos/ajzbc/ajzbc.com');
		const data = await res.json();

		if (res.ok) {
			return data.updated_at;
		} else {
			throw new Error(data);
		}
	}
</script>

{#await getDate() then date}
	{date}
{:catch}
	error
{/await}

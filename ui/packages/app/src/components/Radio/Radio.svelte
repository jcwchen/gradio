<script lang="ts">
	import { Radio } from "@gradio/form";

	export let label: string;
	export let value: string = "";
	export let default_value: string;
	export let style: string = "";
	export let choices: Array<string> = [];
	export let mode: "static" | "dynamic";

	if (default_value) value = default_value;
</script>

<Radio
	bind:value
	{label}
	{style}
	{choices}
	disabled={mode === "static"}
	on:change
/>

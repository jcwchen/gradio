<script lang="ts">
	import { CheckboxGroup } from "@gradio/form";

	export let value: Array<string> = [];
	export let default_value: Array<string> = [];
	export let choices: Array<string>;

	export let mode: "static" | "dynamic";
	export let style: string = "";
	export let label: string;

	if (default_value) value = default_value;
</script>

<CheckboxGroup
	bind:value
	{choices}
	{style}
	{label}
	on:change
	disabled={mode === "static"}
/>

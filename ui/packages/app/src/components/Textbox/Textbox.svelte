<svelte:options accessors={true} />

<script lang="ts">
	import { TextBox } from "@gradio/form";

	export let label: string;
	export let value: string = " ";
	export let default_value: string | false = false;
	export let style: string = "";
	export let lines: number;
	export let placeholder: string = "";

	export let mode: "static" | "dynamic";

	if (default_value) value = default_value;
</script>

<TextBox
	bind:value
	{label}
	{style}
	{lines}
	autoheight={mode === "static"}
	{placeholder}
	on:change
	on:submit
	disabled={mode === "static"}
/>

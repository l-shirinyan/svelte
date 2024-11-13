<script>
	import { twMerge } from "tailwind-merge";

	export let text = "";
	export let type = "button";
	export let isLight = false;
	export let otherStyles = "";
	export let onClick = () => {};
	export let width = "w-full max-w-52";
	export let height = "min-h-10";

	const buttonClasses = twMerge(
		"flex items-center justify-center rounded-lg select-none text-sm hover:opacity-75 active:scale-95",
		isLight ? "border border-gray-border bg-white text-primary" : "bg-primary text-white",
		width,
		height,
		otherStyles
	);
</script>

<button on:click={onClick} {type} class={buttonClasses} aria-label={text || "button"}>
	{text}
</button>

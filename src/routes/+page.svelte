<script lang="ts">
	import { Canvas, Layer, type Render } from 'svelte-canvas';

	let render: Render;
	$: render = ({ context, width, height }) => {
		context.fillStyle = 'red';
		context.fillRect(0, 0, width, height);
	};
</script>

<div class="w-screen h-screen">
	<Canvas>
		<Layer {render} />
	</Canvas>
</div>

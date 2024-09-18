<script>
	import { Protocol } from 'pmtiles';
	import maplibregl from 'maplibre-gl';
	import { onMount } from 'svelte';
	import { base } from '$app/paths';

	const style = `${base}/data/gb-style.json`;

	let protocol = new Protocol();
	maplibregl.addProtocol('pmtiles', protocol.tile);

	onMount(() => {
		// const initialize = { lng: -77.03778, lat: -12.06649, zoom: 13.5 };// Lima
		const initialize = { lng: -5.031075, lat: 53.90009, zoom: 5 }; // Dublin
		const map = new maplibregl.Map({
			container: 'map',
			zoom: initialize.zoom,
			center: [initialize.lng, initialize.lat],
			style: style
		});
	});
</script>

<div id="map"></div>

<style>
	#map {
		position: absolute;
		top: 0;
		bottom: 0;
		width: 100%;
	}
</style>

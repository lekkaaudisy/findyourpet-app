<svelte:head>
	<script defer async
	src="https://maps.googleapis.com/maps/api/js?key=AIzaSyCTPiSivTg1SSaf4jinBaOmQplgU4NWwmM&callback=initMap">
	</script>
</svelte:head>

<script lang="ts">
    let container;
    let map;
    let zoom = 8;
    let center = { lat: -6.75, lng: 107.5 };
  
    import { onMount } from 'svelte';
  
    onMount(() => {
      window.initMap = () => {
        const myLatlng = { lat: -25.363, lng: 131.044 };
  
        map = new google.maps.Map(container, {
          zoom,
          center,
        });
  
        let infoWindow = new google.maps.InfoWindow({
          content: "Click the map to get the address!",
          position: myLatlng,
        });
  
        infoWindow.open(map);
  
        map.addListener("click", (mapsMouseEvent) => {
          const latLng = mapsMouseEvent.latLng;
  
          infoWindow.close();
  
          new google.maps.Geocoder().geocode({ location: latLng }, (results, status) => {
            if (status === "OK" && results && results[0]) {
              infoWindow = new google.maps.InfoWindow({
                position: latLng,
                content: results[0].formatted_address,
              });
              infoWindow.open(map);
            } else {
              console.error("Geocoder failed due to: " + status);
            }
          });
        });
      };
  
      // const script = document.createElement("script");
      // script.src = "https://maps.googleapis.com/maps/api/js?key=AIzaSyCTPiSivTg1SSaf4jinBaOmQplgU4NWwmM&callback=initMap";
      // script.defer = true;
      // script.async = true;
      // document.head.appendChild(script);
    });
</script>
    
<div class="full-screen" bind:this={container}></div>
<div>
</div>
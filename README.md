<!DOCTYPE html>
</html lang="en">
<head> 
  <body>
  </title>
	  <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, 
	    initial-scale=1.0"
<Get-device-location>
</div><Get-device-Internet>
<id="datacontainer"><div>
<script>
	// Fetch data from a JSON API
fetch('https://api.example.com/data')
    .then(response => response.json())
    .then(data => {
        // Display the data on the HTML page
        document.getElementById('data-container').innerHTML = JSON.stringify(data, null, 2);
<h1>Location Access Example</h1>

<button onclick="getLocation()">Get Location</button>

<p id="demo"></p>
<script>
function getLocation() {
    if (navigator.geolocation) {
        navigator.geolocation.getCurrentPosition(showPosition, showError);
    } else document.getElementById("demo").innerHTML = "Geolocation is not supported by this browser.";
    }
}
<script>
function showPosition(position) {
    var latitude = position.coords.latitude;
    var longitude =position.
	    coords.longitude;document.
getElementById("demo").innerHTML = "Latitude: " + latitude + "<br>Longitude: " + longitude;
}
function showError(error) {
    switch(error.code) {
        case error.PERMISSION_DENIED:
            document.getElementById("demo").innerHTML = "User denied the request for Geolocation.";
            break;
        case error.POSITION_UNAVAILABLE:
            document.getElementById("demo").innerHTML = "Location information is unavailable.";
            break;
        case error.TIMEOUT:
            document.getElementById("demo").innerHTML = "The request to get user location timed out.";
            break;
        case error.UNKNOWN_ERROR:
            document.getElementById("demo").innerHTML = "An unknown error occurred.";
            break;  
    } 
}
</script>

</body>
</html>

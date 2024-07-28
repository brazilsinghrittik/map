# Brazil Singh's map
## Use Mapbox to Create Custom Web Maps
![Brazil Singh Map](https://github.com/user-attachments/assets/4224ee14-8c77-41f6-8c5b-4d45d149f85f)

Here is the link to test the map: [Click Here](https://raw.githack.com/brazilsinghrittik/map/main/webmap.html)
### Establish a Connection with Mapbox Resources
Linking the Mapbox JavaScript library and CSS stylesheet into your HTML code is the first step in using Mapbox to generate an online map. Doing this is easy. All we have to do is open an HTML page and include the link to these resources in the <head> section. The most recent versions of the JavaScript library and CSS stylesheet can be found [here](https://docs.mapbox.com/mapbox-gl-js/guides/install/).
### Here is the code of body you can use
 

 ~~~
 <body>
        <script src="https://api.mapbox.com/mapbox-gl-js/plugins/mapbox-gl-directions/v4.1.0/mapbox-gl-directions.js"></script>
        <link rel="stylesheet" href="https://api.mapbox.com/mapbox-gl-js/plugins/mapbox-gl-directions/v4.1.0/mapbox-gl-directions.css" type="text/css">
        <div id="map"></div>
        <script>
            mapboxgl.accessToken = 'your access token';
            const map = new mapboxgl.Map({
                container: 'map',
                style: 'mapbox://styles/mapbox/streets-v11',
                center: [-111, 32],
                zoom: 1
            });

            map.addControl(
                new MapboxDirections({
                    accessToken: mapboxgl.accessToken
                }), 'top-left'
            );

            map.addControl(new mapboxgl.NavigationControl()); 
        </script>

    </body>
~~~

### Here is the Header Section
~~~
 <head>
        <title>Brazil Singh Map</title>
        <meta name="viewport" content="intial-scale=1,maximum-scale=1,user-scalable=no">
        <link href="https://api.mapbox.com/mapbox-gl-js/v2.10.0/mapbox-gl.css" rel="stylesheet">
        <script src='https://api.mapbox.com/mapbox-gl-js/v2.10.0/mapbox-gl.js'></script>
        <style>
            body { margin: 0; padding: 0; }
            #map { position: absolute; top: 0; bottom: 0; width: 100% }
        </style>
</head>
~~~

Or you can copy and run on your vs code and play with the setting for practice purposes!
~~~
<html>
    <head>
        <title>Brazil Singh Map</title>
        <meta name="viewport" content="intial-scale=1,maximum-scale=1,user-scalable=no">
        <link href="https://api.mapbox.com/mapbox-gl-js/v2.10.0/mapbox-gl.css" rel="stylesheet">
        <script src='https://api.mapbox.com/mapbox-gl-js/v2.10.0/mapbox-gl.js'></script>
        <style>
            body { margin: 0; padding: 0; }
            #map { position: absolute; top: 0; bottom: 0; width: 100% }
        </style>
    </head>
    <body>
        <script src="https://api.mapbox.com/mapbox-gl-js/plugins/mapbox-gl-directions/v4.1.0/mapbox-gl-directions.js"></script>
        <link rel="stylesheet" href="https://api.mapbox.com/mapbox-gl-js/plugins/mapbox-gl-directions/v4.1.0/mapbox-gl-directions.css" type="text/css">
        <div id="map"></div>
        <script>
            mapboxgl.accessToken = 'pk.eyJ1IjoiYnJhemlsc2luZ2giLCJhIjoiY2x6NXJtd2ptNGtyNDJtcjR1NWpsYnp0dSJ9.YpnJcw63msNCxqBrw09RuA';
            const map = new mapboxgl.Map({
                container: 'map',
                style: 'mapbox://styles/mapbox/streets-v11',
                center: [-111, 32],
                zoom: 1
            });

            map.addControl(
                new MapboxDirections({
                    accessToken: mapboxgl.accessToken
                }), 'top-left'
            );

            map.addControl(new mapboxgl.NavigationControl());
        </script>

    </body>
</html>
~~~

Link:https://brazilsinghrittik.github.io/map/

<!DOCTYPE html>
<html>
<meta charset="utf-8" />

<head>
    <script src=" https://unpkg.com/leaflet@1.6.0/dist/leaflet.js "></script>
    <link rel="stylesheet" href=" https://unpkg.com/leaflet@1.6.0/dist/leaflet.css" />
    <style>
        #map {
            width: 100%;
            height: 650px;
            box-shadow: 5px 5px 5px #888;
        }
    </style>
</head>

<body>
    <div id='map'>
    </div>
    <script>
        var OMS = L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
            attribution: '&copy; <a href="http://osm.org/copyright">OpenStreetMap</a>'
                + 'contributors',
            maxZoom: 20
        });
        var map = L.map('map', {
            center: [1.61389, -75.6128],
            layers: OMS,
            zoom: 15,

        });
        L.control.scale()
            .addTo(map);
        /*marcador universidad*/
        var marker = L.marker([1.620359549555406, -75.60422170494282], {
            draggable: true,
            title: 'pincha aquí'
        }).addTo(map)
            .bindPopup('Universidad De La Amazonia')
            .openPopup();
    
        /*marcador alcaldia*/
        var universidad = L.marker([1.61507, -75.61384], {
            draggable: true,
            title: 'click aquí'
        }).addTo(map)
            .bindPopup('Alcaldia De Florencia')
            .openPopup();

        /*círculo de la alcaldia*/
        var circle = L.circle([1.61507, -75.61384], 500, {
            color: 'red',
            fillColor: 'red',
            fillOpacity: 0.3
        }).addTo(map);
        var marker = L.marker([1.61493, -75.61326], {
            draggable: true,
            title: 'click aquí'
        }).addTo(map)
            .bindPopup('Plaza Santander')
            .openPopup();

        /*polígono de la plaza*/
        var polygon = L.polygon([
            [1.61515, -75.61364],
            [1.61534, -75.61302],
            [1.61473, -75.61282],
            [1.61454, -75.61345]
        ]).addTo(map)
            .bindPopup('Plaza Santander');
        /*marcador  casa de diego*/
        var marker = L.marker([1.62544, -75.60337], {
            draggable: true,
            title: 'click aquí'
        }).addTo(map)
            .bindPopup('Casa De Diego Linares')
            .openPopup();
        /*marcador  casa de Jhonier*/
        var marker = L.marker([1.621472187708037, -75.59737989215], {
            draggable: true,
            title: 'click aquí'
        }).addTo(map)
            .bindPopup('Casa De Jhonier Gutierrez')
            .openPopup();
        /*De la casa de diego a la universidad*/
        var pointA = new L.LatLng(1.62545, -75.60331);
        var pointB = new L.LatLng(1.62249, -75.60719);
        var pointC = new L.LatLng(1.62249, -75.60721);
        var pointD = new L.LatLng(1.62197, -75.60792);
        var pointE = new L.LatLng(1.62122, -75.60856);
        var pointF = new L.latLng(1.62096, -75.60902);
        var pointG = new L.LatLng(1.62083, -75.60972);
        var pointH = new L.LatLng(1.62081, -75.61001);
        var pointI = new L.LatLng(1.62064, -75.61014);
        var pointJ = new L.LatLng(1.62043, -75.61006);
        var pointK = new L.LatLng(1.62038, -75.60978);
        var pointL = new L.LatLng(1.61957, -75.60749);
        var pointM = new L.LatLng(1.61935, -75.60692);
        var pointÑ = new L.LatLng(1.61851, -75.60634);
        var pointO = new L.LatLng(1.61728, -75.60554);
        var pointP = new L.LatLng(1.61550, -75.60435);
        var pointQ = new L.LatLng(1.61550, -75.60434);
        var pointR = new L.LatLng(1.61536, -75.60431);
        var pointT = new L.LatLng(1.61536, -75.60428);
        var pointW = new L.LatLng(1.61536, -75.60416);
        var pointX = new L.LatLng(1.61546, -75.60412);
        var pointY = new L.LatLng(1.61556, -75.60420);
        var pointY = new L.LatLng(1.61879, -75.60641);
        var pointZ = new L.LatLng(1.62003, -75.60521);
        var pointAA = new L.LatLng(1.62016, -75.60517);
        var pointBB = new L.LatLng(1.62017, -75.60512);
        var pointCC = new L.LatLng(1.62010, -75.60498);
        var latlngs = [pointA, pointB, pointC, pointD, pointE, pointF, pointG, pointH, pointI, pointJ, pointK, pointL, pointM, pointÑ, pointO, pointQ, pointR, pointT, pointW, pointX, pointY, pointZ, pointAA, pointBB, pointCC];
        var polyline = L.polyline(
            latlngs, { color: 'blue' }
        )
            .addTo(map)
            .bindPopup('De la casa de Diego a La Universidad');
        var pointDD = new L.LatLng(1.62154, -75.59736);
        var pointEE = new L.LatLng(1.62147, -75.59662);
        var pointFF = new L.LatLng(1.61874, -75.59701);
        var pointGG = new L.LatLng(1.61859, -75.59725);
        var pointHH = new L.LatLng(1.61854, -75.59769);
        var pointII = new L.LatLng(1.61898, -75.59888);
        var pointJJ = new L.LatLng(1.61900, -75.59924);
        var pointKK = new L.LatLng(1.61852, -75.59999);
        var pointLL = new L.LatLng(1.61866, -75.60009);
        var pointOO = new L.LatLng(1.61930, -75.60152);
        var pointPP = new L.LatLng(1.61973, -75.60247);
        var pointQQ = new L.LatLng(1.61995, -75.60275);
        var latlngs = [pointDD, pointEE, pointFF, pointGG, pointHH, pointII, pointJJ, pointKK, pointLL, pointOO, pointPP, pointQQ];
        var polyline = L.polyline(
            latlngs, { color: 'blue' }
        )
            .addTo(map)
            .bindPopup('De la casa de Jhonier a La Universidad');


    </script>
</body>

</html>

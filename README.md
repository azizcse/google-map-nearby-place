# MapsNearbyPlaces

Learn how to build Android Apps with google maps API that allow user to search nearby places, such as school, hospital, and restaurant. (Android)

## Getting Started

These app can detect nearby places using google places API URL, in this project it will detect nearby schools, restaurant, and hospital.
in this project there is 4 main class:
- DataParser (get all Nearby place data and place a marker on its coordinates)
- DownloadUrl (get URL data using HttpURLConection)
- GetNearbyPlacesData (Get Nearby Place result and save it on HashMap)
- MapsActivity (The Main Activity)

### Code

make sure you connect your project to google API and enable google maps and google place API in console.developers.google.com
add your google maps key on res/values/google_maps_api.xml

the important method on MapsActivity is getUrl

```
private String getUrl(double latitude, double longitude, String nearbyPlace) {
    StringBuilder googlePlacesUrl = new StringBuilder("https://maps.googleapis.com/maps/api/place/nearbysearch/json?");
    googlePlacesUrl.append("location=" + latitude + "," + longitude);
    googlePlacesUrl.append("&radius=" + PROXIMITY_RADIUS);
    googlePlacesUrl.append("&types=" + nearbyPlace);
    googlePlacesUrl.append("&sensor=true");
    googlePlacesUrl.append("&key=" + "YOUR_KEY");
    Log.d("getUrl", googlePlacesUrl.toString());
    return (googlePlacesUrl.toString());
}
```

## Built With

* IDE - Android Studio 2.1.3
* Operating System - Ubuntu

## Authors

* **Marchellin Antonia**

## Screenshot
* first action is locate current location <br />
<img src="https://cloud.githubusercontent.com/assets/12492522/20469982/02a046a2-afd7-11e6-9add-02a0c1776d83.png" width="300">
<br />
* when nearby restaurant button is clicked <br />
<img src="https://cloud.githubusercontent.com/assets/12492522/20469983/02cb3416-afd7-11e6-9b4b-63aa0a22576e.png" width="300">
<br />
* when nearby hospital button is clicked <br />
<img src="https://cloud.githubusercontent.com/assets/12492522/20469984/02eb97a6-afd7-11e6-8bd9-bdcf1c935a1c.png" width="300">
<br />
* when nearby school button is clicked <br />
<img src="https://cloud.githubusercontent.com/assets/12492522/20469985/02ecc3f6-afd7-11e6-8abf-1b90da81d938.png" width="300">
<br />
* when marker is clicked <br />
<img src="https://cloud.githubusercontent.com/assets/12492522/20469986/02ef3d70-afd7-11e6-87a8-76b98a35c12d.png" width="300">


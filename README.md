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




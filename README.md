# Before 1948
[Google Maps]([Demo](https://david90.github.io/before1948/)) listing out private buildings in [Hong Kong](https://en.wikipedia.org/wiki/Hong_Kong) that built before 1948.

## Features

Using Google Maps API and [APITable](https://apitable.co) for a simple demo.

[Demo Map](https://david90.github.io/before1948/)

* Single page example. No external framework besides [Google Maps API](https://developers.google.com/maps/)

![Maps Screenshot](https://user-images.githubusercontent.com/1916493/29515969-2f1a1e50-86a1-11e7-9ab4-e153154461d7.png)

## Data source

* [Private Buildings in Hong Kong Dataset 香港私人大廈數據集](https://bmis2.buildingmgt.gov.hk/bd_hadbiex/content/searchbuilding/building_search.jsf?renderedValue=true)
* [g0vhk.io housing data](http://data.g0vhk.io/group/housing)

## Develop / Deploy your own simple map
This repo is also a great example on how to use [APITable](https://apitable.co) as an easy to set up endpoint of your maps app.

This files are essential for your page:

* index.html - The main map page. You can update the content directly on the page.
* location_24x24.png - The marker image, you may use the default one or your own icon (just replace this image).

#### Important: You shall update your own API Key in your app.
 Replace `XXXXXXXXXXXX ` with your API Key in the code below, located in the bottom most part in `index.html`. Follow the instruction on the [Google Maps Docs](https://developers.google.com/maps/documentation/javascript/adding-a-google-map) to get your own key.

```
<script async defer
src="https://maps.googleapis.com/maps/api/js?key=XXXXXXXXXXXX&callback=initMap">
</script>
```

#### Set up endpoint at APITable

You can define your own data schema according to your usage, however this example follows the following schema on [APITable](https://apitable.co):

1. Sign up at [APITable](https://apitable.co)
2. Add a new table
3. Add columns according to the following
![APITable](https://user-images.githubusercontent.com/1916493/29515974-311d097e-86a1-11e7-90a7-34d97db6cb27.png)

  * Name - `name` Address / Name of the place (Must not be empty)
  * Latitude - `lat` The Latitude of the location
  * Longitude - `long` The Longitude of the location
  * Detail - `detail` Detail of the place.
  * Year Built - `yearbuilt` The year of the building is built.


4. Copy and paste data to the table
5. Click `Save` button to save data
6. Click `Get End Point` button to export an endpoint
7. You need to have a valid token to access to the endpoint, click `creat new token`
8. Click on `view` button next to the new token generated. You will be able to get the URL directly in this format: `https://apitable.skygeario.com/api/tables?id=15414c95-a675-4dec-b29e-165dde8ee59d&token=XXXXXXXX`
9. You can then use this endpoint in your app.

## License
![CC BY](https://licensebuttons.net/l/by/3.0/88x31.png)

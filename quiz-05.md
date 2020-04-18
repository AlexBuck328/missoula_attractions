# Quiz 5

1. Inspect the `hiCraters` object and recognize that the volcanic craters are encoded as an array of objects, a format similar to a GeoJSON. Write a statement that outputs (to the console) the elevation for *Aloi Crater* using the object's dot notation and array index value.

```javascript
      console.log(`The elevation of Aloi Crater is: ${hiCraters.features[2].properties.elevation_ft} feet`);
```

2. What is `byElev()` called?

    >`byElev()` is a method. In the context of the quiz.html, byElev is a property of the object hiCraters. A method is a function that operates only on the data of its associated object. In this case, the `byElev()` method only operates on the data stored in the hiCraters object.

3. Write a statement that shows an example of using `byElev()`.

```javascript
    var craterElev = hiCraters.byElev(10);
    console.log(craterElev);
```

4. Use the `push()` method to add the following crater to the `hiCraters()` object, "Chain of Craters, 3,110 feet above sea level, 19.3709116, -155.185318". Write a JavaScript statement to do this.

```javascript
    hiCraters.features.push({
            "properties": {
                "name": "Chain of Craters",
                "class": "Crater",
                "elevation_ft": 3110,
            },
            "geometry": {
                "type": "point",
                "coordinates": [-155.1853, 19.3709]
            }
        });
        console.log(hiCraters.features);  // to view added crater to hiCraters
```

<!-- Good work on quiz answers! -->

5. Bonus question (+1 pt). Add code to the [quiz.html](quiz.html) file that maps the craters listed in the result of question 3 to a Leaflet map.

    > I attempted this, but I was horrendously unsuccessful at getting the markers on the map. I'm unsure how to access the coordinates for the markers, as well as what to put on the marker itself. As a result, I'm not sure I answered question 3 accurately... :/
# Mapping_Earthquakes
# Background
  Basil and Sadhana like how I created my earthquake map with two different maps and the earthquake overlay. Now, Basil and Sadhana would like to see the earthquake data in relation to the tectonic plates’ location on the earth, and they would like to see all the earthquakes with a magnitude greater than 4.5 on the map, and they would like to see the data on a third map.

# **Deliverable 1: Add Tectonic Plate Data**
  Using your knowledge of JavaScript, Leaflet.js, and geoJSON data, I’ll add tectonic plate data using `d3.json()`, add the data using the `geoJSON()` layer, set the tectonic plate `LineString` data to stand out on the map, and add the tectonic plate data to the overlay object with the earthquake data.

Follow the instructions below and the numbered comments in the starter code to complete **Deliverable 1**.

1. Create a new folder on my Mapping_Earthquakes repository and name it "Earthquake_Challenge."

2. Copy the folders and files from your Earthquakes_past7days branch and add them to the Earthquake_Challenge folder. The folder should have this structure:

    - Earthquake_Challenge folder
      - `index.html`
      - static
        - css
          - `style.css`
        - js
          - `config.js`
          - `logic.js`
          
    ![image](https://user-images.githubusercontent.com/112348240/213076032-2fcd8fe9-88de-492c-8985-e8531ea6d29b.png)

3. Download the `tectonic_plate_starter_logic.js` file, add it to your js folder, and rename it `challenge_logic.js`.

    ![image](https://user-images.githubusercontent.com/112348240/213077063-4afc2c31-96b9-46e8-bc81-ed61e80e0411.png)

4. In Step 1, add a second layer group variable for the tectonic plate data.

    ![image](https://user-images.githubusercontent.com/112348240/213077253-ffbfa2c1-1b29-4660-8b04-d8e10bc8db3d.png)

5. In Step 2, add a reference to the tectonic plate data to the overlay object.

    ![image](https://user-images.githubusercontent.com/112348240/213077345-77cb3707-4035-45a9-96a8-d652b3ef9c76.png)

6. In Step 3, using `d3.json()` callback method, make a call to the tectonic plate data using the `GeoJSON/PB2002_boundaries.json` data from this GitHub repository links to an external site.for the tectonic plate data. I’ll need to log into GitHub to access the GeoJSON data.
  
    ![image](https://user-images.githubusercontent.com/112348240/213077509-35f9b00d-ffca-4d94-a516-e6fc81b8a4bb.png)

7. Inside the `d3.json()` method do the following:

   - Pass the tectonic plate data to the `geoJSON()` layer.
   - Style the lines with a color and weight that will make it stand out on all maps.
   - Add the tectonic layer group variable you created in Step 1 to the map, i.e., `.addTo(tectonicPlates)` and close the `geoJSON()` layer.
   - Next, add the tectonic layer group variable to the map, i.e, `tectonicPlates.addTo(map)`.
   - Finally, close the `d3.json()` callback.
   
   ![image](https://user-images.githubusercontent.com/112348240/213078048-26c3f7d9-61dc-4b54-8316-cec7bdd66016.png)

8. Start your Python server and launch the `index.html` file and confirm that my map with the earthquake and tectonic plate data is similar to the following image.

My final map looks similar to the image provide on the Module Challenge:

![image](https://user-images.githubusercontent.com/112348240/213078629-160ccac1-223d-4164-9246-689eeb68d790.png)

# **Deliverable 2: Add Major Earthquake Data**

Using my knowledge of JavaScript, Leaflet.js, and geoJSON data, I’ll add major earthquake data to the map using `d3.json()`. I'll also add color and set the radius of the circle markers based on the magnitude of earthquake, and add a popup marker for each earthquake that displays the magnitude and location of the earthquake using the GeoJSON layer, `geoJSON()`.

Download the `major_eq_starter_logic.js` file and add it to my js folder. Look over the starter code and use it as a template to modify your `challenge_logic.js` file that you used to add the tectonic plate data in Deliverable 1.

Follow the instructions below that refer to the steps in the` major_eq_starter_logic.js` file and make the changes to my `challenge_logic.js` file to complete Deliverable 2.

  1. In Step 1, add a third layer group variable for the major earthquake data.
  
  ![image](https://user-images.githubusercontent.com/112348240/213079442-e6607181-1bed-4331-853b-4a5cec4b060c.png)

  2. In Step 2, add a reference to the major earthquake data to the overlay object.
  
  3. In Step 3, use the `d3.json()` callback method to make a call to the major earthquake data from the GeoJSON Summary Feed for M4.5+ Earthquakes Links to an external site.for the Past 7 Days.
  
  ![image](https://user-images.githubusercontent.com/112348240/213079531-57203486-af5c-43b9-acaf-42084b50848f.png)

  4. In Step 4, use the same parameters in the `styleInfo()` function that will make a call to the `getColor()` and `getRadius()` functions.

  5. In Step 5, change the `getColor(`) function to use only three colors for the following magnitudes; magnitude less than 5, a magnitude greater than 5, and a magnitude greater than 6.

  6. In Step 6, use the same parameters from the preceding step in the `getRadius()` function.
 
  ![image](https://user-images.githubusercontent.com/112348240/213081356-dd064c40-d667-4864-962a-5ad8cad1f8e4.png)

  7. In Step 7, pass the major earthquake data into the GeoJSON layer and do the following with the `geoJSON()` layer:
    - Turn each feature into a circleMarker on the map
    - Style each circle with styleInfo() function
    - Create a popup for the circle to display the magnitude and location of the earthquake
    - Add the major earthquake layer group variable you created in Step 1 to the map, i.e., `.addTo(majorEQ)` and then close the `geoJSON()` layer.

  ![image](https://user-images.githubusercontent.com/112348240/213081408-35b932b0-9cae-4e15-9326-4b622e06601b.png)
  
  8. Then, add the major earthquake layer group variable to the map, i.e, `majorEQ.addTo(map)`, and then close the `d3.json()` callback.

  9. Start my Python server and launch the index.html file and confirm that my map with the two earthquake data sets and tectonic plate data is similar to the image on the challenge.

  ![image](https://user-images.githubusercontent.com/112348240/213082021-88dd98ad-7e37-447d-9490-fac8fc23b2b4.png)

  ![image](https://user-images.githubusercontent.com/112348240/212614745-90f1f15e-5ded-4c4a-8487-a8f9d6b7b61d.png)

  ![image](https://user-images.githubusercontent.com/112348240/212616035-ab2c0453-9947-4270-bdc3-70cf2fbc4d47.png)


# **Deliverable 3: Add an Additional Map**

Using your knowledge of JavaScript and Leaflet.js add a third map style to your earthquake map.

  - Using the options from the Mapbox styles Links to an external site., add a third map style as a tile layer object to the `challenge_logic.js` file.

  - Add the map variable to the base layer object.

  - Start my Python server and launch the index.html file and confirm that your map is similar to the following image, where there are three map styles, and displays the two earthquake data sets and the tectonic plate data.
  
  ![image](https://user-images.githubusercontent.com/112348240/213082921-ac06ae4c-df1a-4573-a786-4fe0e643d5ea.png)

  The legend showing on below screentshoot:
  
  ![image](https://user-images.githubusercontent.com/112348240/213083022-2ca6e421-c0e6-4509-a75d-c794f7ca5f64.png)

# **Sources:**

https://www.mapbox.com/

https://github.com/fraxen/tectonicplates

https://earthquake.usgs.gov/earthquakes/feed/v1.0/summary/4.5_week.geojson

JavaScript, Leaflet.js, and geoJSON data

# **Module 14 Challenge**

**By Marisol Gascon Linarez**

**UCF Bootcamp Data Visualization and Analytics**






# Solar Radiation Analysis
CR Prototyping Project

# Description 
This project aims to utilize the Solar Radiation Analysis to preview how much will the sun affect the facade of the proposed design in a selected location throughout the year.

As a result, architects and users will be able to preview the amount of solar radiation affecting the building based on its orientation, design, shading elements, and location. Users will be able to navigate the map and switch between each month of the year showing the amount of solar radiation on the buildings.

# Importing Dependencies
The code begins with importing necessary dependencies. These dependencies are modules or libraries that contain pre-built functions and components that can be used in the code. In this case, various components and functions are imported from different libraries:

"./App.css"; imports the CSS file associated with the App component.

"./components/ui/resizable"; import resizable components from a custom resizable module in the ./components/ui directory. These resizable components are used for creating resizable panels in the user interface.

Resium is a library that integrates Cesium, a 3D mapping and visualization library, with React. The imported components are used for rendering and interacting with the Cesium map.

Import Cesium from "cesium"; import specific components and objects from the cesium library. Cesium is the core library for working with Cesium. The imported components and objects are used for configuring and manipulating the Cesium map.

"./components/map/GoogleMaps"; imports a GoogleMapsOverlay component from a custom GoogleMaps module in the ./components/map directory. This component is used for overlaying a Google Maps view on top of the Cesium map.

# Initializing Variables and Constants
After importing the necessary dependencies, the code initializes some variables and constants. These variables and constants hold data that will be used later in the component.

The buildingIDs constant is an array of building IDs that has been generated by Cesium.

The BUILDING_COORDINATES constant is an array of latitude and longitude coordinates representing a specific location.

The getResource function is a helper function that takes a building ID as an argument and returns it for the corresponding resource. The resource is retrieved using the cesium access token.

![Screenshot 2024-02-26 215035](https://github.com/Omarabdelaal97/CR_Prototyping_Project/assets/122699912/cc2ac20a-19a6-4750-a000-906f20d81f17)

# App Component
The App component is the main component of the application. It is a functional component defined using the function keyword.

The id state variable holds the currently selected building ID. It is initialized with the first building ID from the buildingIDs array.

The building state variable holds the resource for the currently selected building. It is initialized with the resource corresponding to the initial building ID.

The assignBuilding function is a helper function that takes a building ID as an argument. It updates the id and building state variables with the new building ID and corresponding resource.

The convertIndexToMonth function is a helper function that takes a building ID as an argument and returns the corresponding month name based on the index of the building ID in the buildingIDs array.

![Screenshot 2024-02-26 215106](https://github.com/Omarabdelaal97/CR_Prototyping_Project/assets/122699912/82165666-fece-4f16-85e5-76a243a409ea)

# JSX code

The div element with the class name App serves as the root container for the entire application.

Inside the div element, there are multiple components and elements that make up the user interface, including a title, a dropdown select input, a resizable panel group, a slider input, a checkbox, and a button.

The Viewer component from resium is used to render the Cesium map. It is initialized with various props, including the terrainProvider, clockViewModel, shouldAnimate, and timeline props.

The Cesium3DTileset component from resium is used to render the 3D tileset on the map. It is initialized with the url prop, which specifies the URL of the 3D tileset.

The GoogleMapsOverlay component is used to overlay a Google Maps view on top of the Cesium map. It is initialized with the latitude and longitude props, which specify the coordinates of the location to be displayed.

The ResizablePanelGroup component is used to create resizable panels in the user interface. It is initialized with multiple ResizablePanel components.

The Slider component is used to create a slider input in the user interface. It is initialized with the min, max, step, value, and onChange props.

The Checkbox component is used to create a checkbox in the user interface. It is initialized with the label, checked, and onChange props.

# Steps

To start the App, type 
### "npm i"
in the terminal to download the necessary node_modules. Then after the download is complete, type
### "npm start"
in the terminal which will redirect you to (http://localhost:3000) to view it in the browser.

# Results

Solar Radiation Analysis for 2 different months

![Feb](https://github.com/Omarabdelaal97/CR_Prototyping_Project/assets/122699912/1ef2dd70-041a-4a7c-8d69-334ce84ce526)

![oct](https://github.com/Omarabdelaal97/CR_Prototyping_Project/assets/122699912/06043ae1-4b82-4d50-a70c-75ba15599209)

# Conclusion
In summary, the code imports necessary dependencies, initializes variables and constants, and defines the App component, which serves as the main component of the application. The App component manages state variables, handles user interactions, and renders the user interface. The user interface includes various components and elements, such as a dropdown select input, resizable panels, a slider input, checkboxes, and a button. The Cesium map and Google Maps overlay are also rendered in the user interface.

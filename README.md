# photo-mosaic

Write a Mosaic generator in Javascript that implements the following logic:

1. A user selects a local image file.
2. The app loads that image, divides the image into tiles.
3. The size of each tile defaults to 16x16 pixels but can be changed by adjusting a program code constant.
4. For each tile
    a. Calculate the average colour of the tile
    b. Retrieve a tile of matching average colour from the server
5. Display a photomosaic of the original image using the “average color” tiles retrieved from the server.

Constraints and success criteria:

* the mosaic should be rendered from the top row to the bottom row. That is, the top row should be completely rendered before the second row rendering commences, and so on
* Within a row, tiles can be rendered in any order. 
* The client app should make effective use of parallelism and asynchrony.
* You should use ES6 syntax.
* You are not expected to use any non-core frameworks such as jquery, react or angular.
* You should use npm as the build tool
* Code should be commented, modular and testable.



The project skeleton contains a lightweight server (written in node) for
serving the client app and the tile images. To start it, run npm start.

```sh
    /              serves mosaic.html
    /(js|css)/*    serves static resources
    /color/<hex>   serves an SVG mosaic tile for color <hex>.  
	             	e.g.,   /color/0e4daa
```

The tile size should be configurable via the code constants in js/mosaic.js. The project skeleton is already set up to include those constants in both the mosaic client and the mosaic server.  The default size is 16x16.

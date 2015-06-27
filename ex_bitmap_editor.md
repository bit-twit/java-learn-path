# Exercise - Bitmap Editor

## 1.1 Bitmap average colour.

Write a console program that reads an image (bmp or JPEG) and computes the average color.

### Details

* The file name should be read from console as a parameter.
* Define a ImageStructure Java class that retains all image information: filename, dimensions, BufferedImage Java class.
* The pixel information should be read from the BufferedImage Java class as a matrix of (r,g,b) entities.
* Define a function that receives as parameter the BMP file and returns the ImageStructure class.
* Define a function that receives the ImageStructure and returns a Color class representing the average of the colors in the image's pixel matrix.
* The average will be computed as
`AveragePixelColor(R,G,B)=Color(Avg(<all R's>), Avg(<all G's>), Avg(<all B's>))`
* Print the average to the console.
* Package your application as a JAR.

### Example

`
$ java -jar image_comp_average.jar image.png
;;=> (233,204,123)
`

### Further reading

* Working with images in Java - http://docs.oracle.com/javase/tutorial/2d/images/index.html

## 1.2 Bitmap grayscale

Build a console program that reads a coloured image and saves it in grayscale form.

### Details

* Use the image_comp_avg.jar defined above to read the image; add the JAR as dependency to your new project.
* Build a function that takes as parameter a ImageStructure object and saves it, returning a boolean indicating if the save was successful or an error occured.
* Test that your save works: load an image and save it and then compare them to make sure they look the same; compare sizes also.
* Build a function that takes as parameter a ImageStructure and applies grayscale transform on it, returning a new ImageStructure.
* Apply your grayscale function to the inital image.
* Save the image to disk.
* Check out the result.
* Compare your result with a grayscale image obtained from an image manipulation software.
* Package your application as JAR.

### Example

`
$ java -jar image_grayscale.jar initial_image.jpg
;; => Results written to grayscale_image.jpg
`

### Further reading

* Grayscale transform - http://www.johndcook.com/blog/2009/08/24/algorithms-convert-color-grayscale/

## 1.3 Swing image editor

Build a Swing interface that allows 2D image manipulation: load image, save image, apply grayscale transform on the image.

### Details

* Build a JFrame interface with a menu to load/save image.
* After image loading draw the image on a 2D Canvas.
* Add a menu entry for Transformation with a Grayscale child menu.
* Use the functions defined in the above JARs to add actions to menu entries.
* When a Transformation is applied show the results in realtime in the Canvas.
* Maintain the state of the Canvas in memory (clean/dirty) and add a Dialog to ask the user to save the modified image on exit.
* Package your application as an executable JAR, so you can run it with 2click (at least on Win, not sure if that works on Linux).

### Further reading

* Working with images -  http://docs.oracle.com/javase/tutorial/2d/images/index.html
* Working with Frames - https://docs.oracle.com/javase/tutorial/uiswing/components/frame.html
* Working with Menus - https://docs.oracle.com/javase/tutorial/uiswing/components/menu.html
* Working with Dialogs - https://docs.oracle.com/javase/tutorial/uiswing/components/dialog.html

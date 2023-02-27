# RTI-How To Setup CAM in Fusion360
<p float="center">
  <img src= "img\Fusion360-Logo.png" height="32%" />
  <img src="img\Amana-Tools-Logo.png" hieght="32%" /> 
  <img src="img\Carbide3D-Logo.png" height="32%" />
</p>

## Prerequisit Items:
Download a free copy of Fusion360 from [here](https://www.autodesk.com/education/edu-software/overview?sorting=featured&filters=individual).

## How to Setup Parts for CAM:

    1. Open Fusion360.

    2. Open a new file in Fusion.

    3. Realign the prespective such that the 'Front' of the piece is facing the positive X-axis, and the 'Top' is facing the positive Z-axis.

      a) Hover over the prespective cube on the top-right.

      b) Right-Click the face of the cube facing the positive Z-axis.

      c) In the pop-up, select 'Set as Top'.

      d) Right-Click the face of the cube facing the positive X-axis.

      e) In the pop-up, select 'Set as Front'.

This step is to ensure that later in the CAM setup, the work material's axes are naturally facing the correct directions. This is not strictly necessary, however, it does simplfy the process and ensures consistancy.

    4. Save the file and give it a name.

    5. Create a new Sketch on the XY plane.

    6. Measure you the material you want to cut, and create a rectangle or shape with the same dimensions of the material.

The rectangle/shape you draw in the sketch will act as a ```Bounding Box```. We will use this as a conveniant way to lineup parts in the work material, and ensure that all parts have enough room for cutting.

You can optionally draw in areas you want to place work holding to help visualize the cutting area and avoid crashes.

```When doing this step remember to take into consideration that the material might have already been used, so create small shapes in the sketch to account of those used parts.```

    7. DOUBLE CHECK THE MATERIAL'S DIMENSIONS!

```Incorrect measurements may result in a failed cut and a HIGH likeliness of damaging the machine. Besure also to check if you are using the correct units. Metric or Imperial Units!```

    8. Once dimensions are confirmed, exit the sketch.

    9. Import parts to be cut as new components.

      a) Find the part to be cut from the files list in the Data Panel.
      ***If you can't find the Data Panel, or you have hid it, you can access it with the 3x3 grid icon on the Top-Left Corner.

      b) Right-Click the part you want.

      c) In the Drop-down panel, select 'Insert into Current Design'.

      d) Hit 'Ok', in the popup window on the right, or press 'Enter' on your keyboard.

      e) Do steps b) and c) for all parts you want to cut with this material.

    10. In the main workspace. Select the 'MODIFY' tab.

    11. In the dropdown window. Select 'Align'.

    12. In the window on the right. Select the 'Object' dropdown and switch to Components.

    13. Select the box next to 'From' and select a face on the part.

    14. Select the box nect to 'To' and select the sketch from Step 5).

    15. Click 'Ok' in the Window.

    16. Do Steps 10) to 15) for all parts.

```Be sure to one face from each part to face be flat against the sketch's plane. All parts should be under the sketch's plane, and have one face touching the plane.```

    17. Set the current view to be 'Top" view.

    18. Click and drag the parts along the plane to organize them across the workpiece.

```Make sure that there is a minimum of 3/8in or 9mm of clearence between the edge of the work material and parts FOR ALL EDGES OF THE MATERIAL.``` This is to ensure that there is room for workholding and to minimize the chance of crashing. 

```Do not group parts to tightly.``` The CNC milling process is a subtractive process, meaning it eats away materials. ```Be sure to have a MINIMUM of 2.5x the Outter Diameter of largest used endmill bwteen parts.``` If they are too close the part may cut into one another.

    19. Double check if any parts are too close to the edge, or if any parts are too close together.

    20. Delete any remaining parts that you couldn't find room for on the material.

    21. Save the file.


## How to Setup CAM:

    1. In the dropdown on the the top left, labeled: 'Design', select 'Manufacturing'.

    
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
<p float="center">
  <img src= "img\How_To_Setup\3a.png" width="50%" />
</p>

      b) Right-Click the face of the cube facing the positive Z-axis.
<p float="center">
  <img src= "img\How_To_Setup\3b.png" width="50%" />
</p>

      c) In the pop-up, select 'Set as Top'.
<p float="center">
  <img src= "img\How_To_Setup\3c.png" width="50%" />
</p>

      d) Right-Click the face of the cube facing the negative Y-axis (Positive X-axis acing right and Positive Z-axis facing up).
<p float="center">
  <img src= "img\How_To_Setup\3d.png" width="50%" />
</p>

      e) In the pop-up, select 'Set as Front'.
<p float="center">
  <img src= "img\How_To_Setup\3e.png" width="50%" />
</p>

      ***Steps d) and e) can be skipped if the 'front' position had already been set correctly.888

This step is to ensure that later in the CAM setup, the work material's axes are naturally facing the correct directions. This is not strictly necessary, however, it does simplfy the process and ensures consistancy.

    4. Save the file and give it a name.

    5. Create a new Sketch on the XY plane.
<p float="center">
  <img src= "img\How_To_Setup\5.png" width="50%" />
</p>

    6. Measure you the material you want to cut, and create a rectangle or shape with the same dimensions of the material.
<p float="center">
  <img src= "img\How_To_Setup\6.png" width="50%" />
</p>

The rectangle/shape you draw in the sketch will act as a ```Bounding Box```. We will use this as a conveniant way to lineup parts in the work material, and ensure that all parts have enough room for cutting.

You can optionally draw in areas you want to place work holding to help visualize the cutting area and avoid crashes.

```When doing this step remember to take into consideration that the material might have already been used, so create small shapes in the sketch to account of those used parts.```

    7. DOUBLE CHECK THE MATERIAL'S DIMENSIONS!

```Incorrect measurements may result in a failed cut and a HIGH likeliness of damaging the machine. Besure also to check if you are using the correct units. Metric or Imperial Units!```

    8. Once dimensions are confirmed, exit the sketch.
<p float="center">
  <img src= "img\How_To_Setup\8.png" width="50%" />
</p>

    9. Import parts to be cut as new components.

      a) Find the part to be cut from the files list in the Data Panel.
      ***If you can't find the Data Panel, or you have hid it, you can access it with the 3x3 grid icon on the Top-Left Corner.

      b) Right-Click the part you want.

      c) In the Drop-down panel, select 'Insert into Current Design'.

      d) Hit 'Ok', in the popup window on the right, or press 'Enter' on your keyboard.

      e) Do steps b) and c) for all parts you want to cut with this material.

<p float="center">
  <img src= "img\How_To_Setup\9.png" width="50%" />
</p>

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

    2. Right Click the 'Setups' box in the top left of the work space.
    3. In the dropdwon tab, select 'New Setup".

    4. Be sure that in the 'Setup' Section, that the operation type is set to 'Milling'

    5. In the new Setup tab on the right, select the 'Select' box in the 'Model' section of the tab.

This should create an automatic bouding box around all your parts.

    6. In the 'Work Coordinate System (WCS)' section, click the box next to 'Stock Point'.

    7. Points will appear on the bounding box. Select the TOP LOWER LEFT corner point.

```BE SURE that the point selected is the point in the TOP LOWER LEFT point of the work piece.``` This should be the point with the positive Z-axis facing up, the positive X-axis facing right, and the positive Y-axis facing towards the back.

    8. Double check the correct point has been selected, and thtat all pieces are selected.

    9. In the top of the Setup window, switch to the 'Stock' tab.

    10. In the 'Mode' option, select 'Fixed sized box'.

    11. Re-measure the dimensions of the material to cut.

    12. Set the values in the 'Width(X)' and 'Depth(Y)' options to the dimensions of the material to cut.

    13. Set the 'Model Position' of 'X' to 'Offset from left side(-X)'.

    14. In the new 'Offset' section, set the value to "0.375in".

    15. Set the 'Model Position' of 'Y' to 'Offset from front side(-Y)'.

    16. In the new 'Offset' section, set the value to "0.375in".

    17. Set the value for 'Height(Z)'.
        a) To get the Z hieght of the material, use calipers to measure EACH corner of the material.

        b) Use the measurement of the corner Closest to the all the parts laid out on the sheet, or the one with the lowest value.

    18. Set the 'Model Position' of 'Z' to 'Offset from top (+Z)'.

    19. In the new 'Offset' section, set the value to "0in".

    20. In the top of the Setup window, switch to the 'Post Processing' tab. 

    21. Under the 'Machine WCS' section, set 'WCS offset' to "1".

    22. Double check all previous steps.
```WARNING: Most potential CNC crashing and cutting issues can stem from incorrectly inputs during the New Setup process.``` Double checking this section is ```CRUCIAL``` to ensuring safe operation and minimize damage to the machine.

    23. Click 'OK' at the bottom right of the window.

    24. An error may popup saying that the parts exceed the Z-Height, you can ignore it and click 'OK'.

This tutorial is mainly focused on CNCing for 2D parts and operations. 2.5D and potential 3D operations will be explored in later chapters.

    25. Under the 'Setups' folder, there should be a new folder with the name of the new setup you just made.

    26. Right Click the new setup, hover over 'Create from Template' in the popup, and Click 'Select Template'.

    27. In the 'Template Library' window, select the template with the correct material and appropriate material thickness.

    28. The selected tempalte should change color. Once selected, Click 'Select' on the bottom right in the window.

    29. This should create a series of operations under the setup folder.

These new operations are the cutting instructions that the CNC will read during cutting. They will all contain a red error symbol on them at initial import. This is because the operations are not assigned to anything yet. We will explore how to resolve this in [How to use templates](How_To_Use_Templates).
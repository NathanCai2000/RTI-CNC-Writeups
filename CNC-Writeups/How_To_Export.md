# RTI-CNC How to Export Your CAM
<p float="center">
  <img src= "img\Fusion360-Logo.png" height="32%" />
  <img src="img\Amana-Tools-Logo.png" hieght="32%" /> 
  <img src="img\Carbide3D-Logo.png" height="32%" />
</p>

## Prerequisit Items:
  This assumes you have a CAM setup completed and ready for export.


## How to export CAM from Fusion360:
    1. Under the 'Setups' folder, Right Click the setup you want to export.

    2. Select 'Post Process'.

    3. In the new window, under 'Post', select in the drop down window, 'Choose from library...'.

    4. In the dropdown on the the top left, labeled: 'Design', select 'Manufacturing'.

    5. In the new window, under folder 'Fusion 360 library', find the option with Vendor: 'Carbide 3D' and Description: 'Carbide 3D (Grbl)'

    6. Once the correct post processor is selected, Click 'Select'.

    7. A pop-up window might appear named 'Use post from Fusion 360 Library'. If this appears:

        a) Select the drop-down window, and select 'Choose another location...'.

        b) In the new window, under 'My Posts', select 'Local'.

        c) Click 'Select'.

        d) Then select 'Copy to My Posts' once back in the previous window.

    8. Under program, give the new file a name.

```This name can be anything, however, placing some information in the name would be useful.``` Items such as: Name, Material Thickness, Material, 2D/ 2.5D/ 3D operation, iteration, etc.

    9. Select the Output Folder.

You can view the output folder using the other file with an eye icon

    10. Once the previous steps have been completed, select 'Post'.

The final gcode should now be posted to your selected Output folder. This is now the completion of the Beginner tutorial to CAM using RTI's premade templates. Please proceed to the next chapter on how to run the CNC with the gcode. [See Chapter 3](README.md)
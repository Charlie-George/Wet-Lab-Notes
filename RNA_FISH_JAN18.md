RNA FISH Notes 
==============






Microscope
==============

YOu can get instructiions for the zippy microscope here:
http://www.sussex.ac.uk/gdsc/intranet/pdfs/DeltaVision%20Core%20and%20personal%20DV%20Users%20Manual_D.pdf

**Turning it on**
-----------------

1. Make sure objective lens are at thier lowest point (*turn coarse focus away from you*)
2. Turn the computer on - round button above green and blue lights (see the instructions on the wall for reminder of where the buttons are)
3. Turn on the power strip (red button)
4. Switch on the lk mic (green round button)
5. Pull out the keyboard from under the desk
6. Log on 
7. Open SoftWorx software 
8. File - Aquire Resolve 3D 
9.**MAKE SURE OBJECTIVES ARE AT LOWEST POINT**
10. Click initialize -> software will open up


**Placing your slide on the Microscope** 
-----------------------------------------
If its your first sample or you don't have many cells you might need to do the following to find the right focus 


1. Manually select 20x objective lens 
2. If the stage is not on the microscope - screw this in - you might need to gently lift up the condensor
3. Turn off the light
4. Gently place slide upside down over the objective (so the coverslip is on the bottom) making sure it is level and secure
5. Adjust the stage location so that it is pointing at D or E (this should make sure that your objective is in the right possition for your coverslip)
6. Use the joystick to move the slide so that the coverslip is directly above the objective
7. Place the condensor gently down
8. Make sure the dial choosing eyepiece or camera is turned to eyepiece 
9. Check the eyepeice filter (ep) is on DAPI - if not use the front wheel to set light on DAPI, Cy5, TritC etc (Ex, Em, (Ep = eyepiece) should all show the same)
  - NB: POL = Brightfield
  - Cy3 = TRITC
10. Set %T to 10%

11. press the "EX" button on the keypad to turn on dapi emmision (390/18)
12. look through eyepeice and move objective up towards sample by moving it upwards (rotate wheel towards you) so that you focus on your very very tiny blue cells - maybe too tiny to see at this point but you should be able to focus the blue color - you are now in the right possition so that you can switch to the oil objectives and image your sample. It can help to move around the stage 
13. Turn off the excitation by pressing "EX" button

**Switch to the oil objective**
--------------------------------
1. remove your slide 
2. Manually select the correct objective (100x 1.40? - the magnification is 100x but the resolution in 1.40, the higher the aperture number the better the resolution. The 60x has a apperture of 1.45 so this will actually give you better resolution then the 100x and you can also use the aux lens to increase 60x by 1.6x )
3. Put a drop (~3mm diameter) of immersion oil with refractive index 1.514 carefully onto the center of the objective without letting the glass rod touch the lens- rotate the dropper while holding it to prevent the oil falling off if there is alot of oil on the dropper let a drop fall off it first.
4. Place your slide carefully back onto the stage 
6. Turn on the "EX" button 
7. Focus your cells using the eyepiece - move downwards (towards the wall first, then upwards) the closer you are to your cells the more intense the blue from the DAPI 
8. Turn off the EX button


**Setting up softworx software**
--------------------------------

To find the ideal exposure times for different dyes/samples use the expsoure time for your most strongly expressing sample

**For each dye find the ideal exposure:** 
1. Make sure the dial under the eye piece is set to "camera" when acquiring images 
2. Select the appropriate filter DAPI, Cy5, TritC etc (Ex, Em, (Ep = eyepiece) should all show the same)
  - NB: POL = Brightfield
  - NB TRITC = Cy3
  - if you need to change the filters (e.g. using synthetic(GFP) rather then organic (Cy3/DAPI) filters you can do this by clicking on the settings cog/files/Selectfilters - make sure you click ACTIVATE!
3. Set Neutral density Value (%T) - start at 100% but it will depend on what you are imaging and the strength of your probe - you might be able to decrease it for very strong signals
4. In Resolve 3D polychroic should be set to quad --- NOT SURE WHAT THIS IS DELETE? 
5. 'Illumination' should be set to EX (excitation) 
6. Image size (start at 1024x1024) 
7. Set "Lens" to 100x1.35 (or 1.40 if they have it) 
8. Set "Bin" to 1x1
9. uncheck the "Aux Max" box if you are not using it (this is the push out lever on the right hand side of the microscope that lets you increase the magnification by 1.6x)
10. Set the exposure to a low value e.g 0.1sec
11. Center on the image using the target symbol 
12. Set dZ to the desired value to sample differnt images through the sample
13. Click the dZ testbox and enter deired value for z step e.g. 0.2um 
14. Click Aquire through different z sectopm to get maxium focus = tjos will be the place with the highest maximum intensity value 
15. Click find to automatically select a exposure time (for low signals it is fine to have a lower range but for strong signals you do not want to saturate it - have a max value of 3666 which is well below the actual top value of 4095) 
16. **Make a note of the exposure time - round it to the nearest number!! Use this for all samples in the experiment**
17. Repeat above for each filter - using the most strongly expressing sample! 

Once you have got your exposure conditions you can set up your experimental run. 



Select z stack - 
  - move trough sample to find top and bottom - mark with the appropritate buttons t
  - use the arrow to possition yourself in the middle of the zstack - mark point - markpoints will remember this as the middle of the zstack 
  - click the lens button on the resolve3D window to open the lens information box and use the value in the *Recommended Z Step size* field
  - click get thickness to calculate the number of sections you need 


TIPS
=====
- **Moving around the stage**
  - you can use the buttons on the keypad to move in steps by X, Y, and Z directions 
  - The size of each step is doubled each time by the STEP INCREASE button and halved each time the STEP DECREASE button.
  - you can adjust the stepsize to the frame size so that each step arrow will move one frame so you can scan large areas easily


What is deconvolution 
  - computational intensive image processing techicque to imrpove contrat and resolution - it removes or reverses the blurring from limited apertures 
  - ENABLES WIDEFIELD MIRCROSCOPES TO HAVE SAME RESOLUTION AS CONFOCALS 
  - Removes
      - Noise = can be removed in preprocessing as well understood
      - Scatter = depend on thickness 
      - Blur = removed by deconvolution = signal spreading (point spread function)
      - Glare 
  
  
Z Sectioning
  - If have used an overscan method to make sure you get all the nessecary z-section  cut out the unecessary ones during deconvolution by specifying the section numbers of the Z start and Z end 

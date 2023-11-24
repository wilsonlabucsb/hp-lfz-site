# Imaging control

![](../img/focus.png)

## Camera

The camera views the sample through window 1 on the chamber. The software "Pylon Viewer" is used to view live video feed from the camera. Once Pylon Viewer is open, navigate to Window > Devices > Basler acA1300-75gc. In the top left, click the power on button.

Then click the video recorder button.

Image should appear.

To adjust exposure (brightness) go to Window > Features - All > Acquisition Controls > Exposure Time (ms).

To adjust focus, twist knob on camera

To adjust shutter aperture (brightness) manually turn the front tab knob on the camera.

To further dim the brightness use a neutral density (ND) filter which you can slide.

## Pyrometer

The pyrometer views the sample through window 4 on the chamber. The software "DataTemp MultiDrop" is used to view the video feed and get pyrometry (temperature) readings.

The brightness / exposure time is automatically controlled by the pyrometer software, it cannot be manually adjusted.

The focus of the pyrometer is controlled by the front knob on the pyrometer housing.

## Recommended imaging settings for aiming beam:
- Exposure Time (ms) = 100,000
- Pyrometer filter = No notch filter
- Camera filter = No ND filter, shortpass filter optional
- Aiming beam on for lasers 2, 3, 5, 6, and 7. (Not lasers 1 and 4 where the camera and pyrometer are)

## Recommended imaging settings for infrared beam:
- Exposure Time (ms) = 100 to 20,000
- Pyrometer filter = Notch filter in place
- Camera filter = ND1, ND2, or ND4 in place, in addition to shortpass filter.


![](../img/filters.png)

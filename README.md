<img src = "https://github.com/drmartens/arJamMIT/blob/master/demoImage.JPG" width="50%">
# AR Music Hackathon
This is a demo project for the Parsons/MIT Media Lab/Berklee School of Music Augmented Reality + Music Hackathon/Workshop weekend in January 2018.

## What Does it Do?
This is an A/R project that waits for 4 triggers to be present on camera and plays an orchestral movement when the condition is fulfiled.

## What is this part of?
This is part of a larger demo project our team created to explore how we might add to the pre and post concert experience for the OAE Orchestra. The first part of this demo is a Unity phone app that allows users to find pieces of musical instruments hidden around a space by using their phone to scan A/R trigger images (pieces of instruments), listen to a short musical phrase, and collect the instrument part if it is needed to complete their chosen instrument. Once a user has completed building an instrument through the Unity app, they will receive a symbol for the completed instrument. They must then find 3 other users with different instrument symbols to complete their band. Once a band is created, they can bring their instrument symbols to a central display where this A-Frame and Ar.js app will scan the 4 symbols and play the full orchestral movement.

## App Features
* Uses Ar.js custom markers to check if instrument symbol is present
* When all 4 markers are detected, plays orchestral movement

## Libraries & Resources Used
* A-Frame
* AR.js
* Python Simple Server to resolve CORS issues
* Adobe Illustrator for creating Trigger Images and the Instrument Patterns. Each pattern is used as material for a Cube that appears when the instrument trigger symbol is detected by the camera.

## Notes
In order to get the custom markers to work, I first needed to follow [these instructions](https://github.com/wimvdc/AR.js/commit/950e82db6d0c3851647d429282c5ade52ee95891) to modify the code base of the AR.js library to allow for custom marker presets.You must include the Ar.js library saved in this folder, it will not work with a remote add in from their most current source. 

I also used a [custom script from Don Mccurdy](https://github.com/donmccurdy/aframe-extras/issues/180) to register separate components for each of the 4 markers so that their appearance on camera could act as an event trigger since this is not natively part of the AR.js app. This code is included in the index.js file.

The image markers are little trick as a-frame isn't quite as good as apps like Vuforia for registering custom images as markers. To use a custom marker, create a simple image, save as JPG or PNG and use the Ar.js Custom Marker Creator to create a pattern (.patt) file to train the program on this image. These .patt files must be included in the build for the images to work.

## Trigger Images
Here are the trigger images if you want to try this app out.

Bassoon
![bassoonTrigger](https://github.com/drmartens/arJamMIT/blob/master/imageTriggerPhotosforTesting/bassoonTrigger.png)


Oboe
![oboeTrigger](https://github.com/drmartens/arJamMIT/blob/master/imageTriggerPhotosforTesting/oboeTrigger.png)


Viola
![violaTrigger](https://github.com/drmartens/arJamMIT/blob/master/imageTriggerPhotosforTesting/violaTrigger.png)


Violin
![violinTrigger](https://github.com/drmartens/arJamMIT/blob/master/imageTriggerPhotosforTesting/violinTrigger.png)




![demo image](https://github.com/drmartens/arJamMIT/blob/master/demoImage.JPG)

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

## Notes
In order to get the custom markers to work, I needed to follow instructions from StackExchange to modify the code base of the AR.js library to allow for custom marker presets. You must include the Ar.js library saved in this folder, it will not work with a remote add in from their most current source. I also needed to write custom script to listen for each marker as an event trigger since this is not natively part of the AR.js app. This code is included in the index.js file.

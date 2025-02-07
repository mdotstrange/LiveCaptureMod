# LiveCaptureMod
Modified version of Unity's Live Capture package for production of "I'm living my life"

Info-

(On Mac)
Make a Unity account + Download + Install Unity
https://id.unity.com/account/new
Choose to install Unity 2022 or 2021

(On Phone)
Install Face Capture onto your device and plug device into computer via USB
Allow incoming connections to/from the device/computer/Face capture
Launch the Face Capture App on your device

(In Unity)
Install ARKIT package from package manager
Import LiveCapture custom package I provide(ignore red text errors about missing pngs)
Go to Window--> Live Capture--> Connections and dock that window to a tab behind the inspector-- click create server(companion server etc)
Double click the scene file in LiveCapture/ARKit Face Sample/FaceCaptureSample.unity
You will see a head- move the viewport around so you can see it well- put the game tab somewhere else not behind the Scene view
Press the PLAY button at the top middle of the screen

(On Phone)
Look at the Face Capture App on your device, it should list your computer name- connect to it
Now your face should be mapped to the sample face
(Sometimes you need to try this a few times for it to connect/work)

(On Unity)
Locate the TakeRecorder object in the Hierarchy
Locate the Audio Source component on that object in the Inspector
Drag/drop the audio file you want to work with into the AudioClip field
Now when you press Start Recording on the Take Recorder in the Inspector it will start recording and autoplay the audio file
It till automatically stop recording when the audio file is done
It will save your takes in a new folder named appropriately
You don't have to worry about naming or messing with any of that
Do as many takes as you like for each audio file
When finish you will see a "Takes" folder in your Project window- that is the folder you will give to me when you're done

# Live capture notes

* Live capture playback at runtime won't work in Slate if the actor has an Animation Controller loaded into its Animator component
* The head rotation won't play back at runtime so add additional ARKITHeadBone as a parent of the head bone and rotate this new one
* Use soft interpolation on a custom evaluator for more realistic blendshape animation
